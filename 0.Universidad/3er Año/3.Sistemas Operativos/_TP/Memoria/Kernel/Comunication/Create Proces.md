# Request To Memory
```go
type RequestToMemory struct {  
    Thread    Thread  
    Type      string   `json:"type"`  
	// [archivo_pseudoCódigo, tamaño]    
    Arguments []string `json:"arguments"`  
}
```

1. Lee el archivo de speudo codigo y los guarda en el slice del thread apropiado
2. Asigna partición al proceso 
3. Le crea un contexto y lo guarda 
```go
func CreateProcessHandler(w http.ResponseWriter, r *http.Request) {  
    // Leer el cuerpo de la request  
    var requestData types.RequestToMemory  
    err := json.NewDecoder(r.Body).Decode(&requestData)  
    // Extraer el PID y el tamaño desde el cuerpo JSON  
    pid := requestData.Thread.PID  
    mainThread := types.Thread{  
       PID: pid,  
       TID: types.Tid(0),  
    }  
    size, _ := strconv.Atoi(requestData.Arguments[1])  
    pseudoCodigoAEjecutar := requestData.Arguments[0]  
  
	// LEE EL ARCHIVO DE SPEUDO CODIGO 

    file, err := os.Open(pseudoCodigoAEjecutar)  
    if err != nil {  
       logger.Error("No se pudo abrir el archivo de pseudocódigo - %v", err)  
    }  
    defer file.Close()  
    scanner := bufio.NewScanner(file)  
    if scanner == nil {  
       logger.Error("No se pudo crear el scanner")  
    }  
  
    for scanner.Scan() {  
       instructionRead := scanner.Text()  
       if isNotAnInstruction(instructionRead) {  
          continue  
       }  
       memoriaGlobals.CodeRegionForThreads[mainThread] = append(  
          memoriaGlobals.CodeRegionForThreads[mainThread], instructionRead)  
    }  

	// ASIGNA PARTICIÓN AL PROCESO 
	
    base, err := memoriaGlobals.SistemaParticiones.AsignarProcesoAParticion(types.Pid(pid), size)  
    if err != nil {  
       logger.Warn("No se pudo asignar el proceso < %v > de tamaño %v a una particion de memoria", pid, size)  
       if err.Error() == types.Compactacion {  
          logger.Debug("Se debe compactar")  
          w.WriteHeader(http.StatusConflict)  
          return  
       }  
       w.WriteHeader(http.StatusInternalServerError)  
       return  
    }  

	// CREA EL CONTEXTO DEL PROCESO 

    logger.Trace("MemoryBase: %v; MemorySize: %v", base, size)  
    context := types.ExecutionContext{}  
    context.MemoryBase = base  
    context.MemorySize = uint32(size)  
  
    memoriaGlobals.MutexContext.Lock()  
    memoriaGlobals.ExecContext[mainThread] = context  
    memoriaGlobals.MutexContext.Unlock()  
  
    logger.Info("Contexto creado para el hilo - (PID:TID): (%v, %v): %v", pid, 0, context)  
  
    // Log obligatorio  
    logger.Info("## Proceso Creado - PID: < %v > - Tamaño: < %v >", pid, size)  
  
    w.WriteHeader(http.StatusOK)  
    _, _ = w.Write([]byte("Proceso creado correctamente"))  
}
```