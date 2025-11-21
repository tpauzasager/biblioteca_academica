# Init 
Va iterando por la lista de particiones de la config y va creando las particiones con los tamaños de la config 
```go
func (f *Fijas) Init() {  
    base := 0  
    for _, tamanio := range memoriaGlobals.Config.Partitions {  
       particion := memoriaTypes.Particion{  
          Base:    base,  
          Limite:  base + tamanio,  
          Ocupado: false,  
       }  
  
       f.Particiones = append(f.Particiones, particion)  
  
       base += tamanio  
    }  
}
```

# AsignarProcesoAParticion
A partir de la estrategía de asignación, devuelve la base de la partición encontrada que tenga capacidad requerida
```go
func (f *Fijas) AsignarProcesoAParticion(pid types.Pid, size int) (base uint32, err error) {  
    err, particionEncontrada := memoriaGlobals.EstrategiaAsignacion.BuscarParticion(size, &f.Particiones)  

	// Setea los atributos de la partición ahora ocupada 
    particionEncontrada.Ocupado = true  
    particionEncontrada.Pid = pid  

    return uint32(particionEncontrada.Base), nil  
}
```

# Liberar Particion
Recibe un PID y, luego de encontrar la partición (iterando por todas las particiones existentes), setea los atributos para indicar que está libre 
```go
func (f *Fijas) LiberarParticion(pid types.Pid) error {  
    encontrada := false  
    for i := range f.Particiones {  
       particion := f.Particiones[i]  
       if particion.Pid == pid {  
          f.Particiones[i].Ocupado = false  
          f.Particiones[i].Pid = 0  
          encontrada = true  
          logger.Debug("Particion encontrada: Base: %v", particion.Base)  
          break  
       }  
    }  
    if !encontrada {  
       return fmt.Errorf("no se encontro particion que contenga el proceso PID: < %v >", pid)  
    }  
    return nil  
}
```

# Obtener Particion de Proceso
Recibe PID y busca cual es la partición con el atributo PID igual al recibido 
```go
func (f *Fijas) ObtenerParticionDeProceso(pid types.Pid) (memoriaTypes.Particion, error) {  
    for _, particion := range f.Particiones {  
       if particion.Pid == pid {  
          return particion, nil  
       }  
    }  
    return memoriaTypes.Particion{}, fmt.Errorf("no se encontro una particion con el proceso PID: %v", pid)  
}
```