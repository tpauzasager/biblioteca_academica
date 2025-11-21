```go
	// Recibe el Thread y el PC por query param
	tidS := query.Get("tid")  
	pidS := query.Get("pid")  
	pcS := query.Get("pc")  

	// Parsea lo recibido 
	tid, err := strconv.Atoi(tidS)  
	pid, err := strconv.Atoi(pidS)  
	pc, err := strconv.Atoi(pcS)  

	// Crea el dato Thread 
	thread := types.Thread{PID: types.Pid(pid), TID: types.Tid(tid)}  
	  
	// Obtener la instrucción según el PC  
	instruccion, err := helpers.GetInstruction(thread, pc)
```

# helpers.GetInstruction
```go
func GetInstruction(thread types.Thread, pc int) (instruction string, err error) {
	// Obtiene el listado de instrucciones del Thread
	instructions, exists := memoriaGlobals.CodeRegionForThreads[thread]  
	  
	// Verificar que el PC está dentro de los límites de las instrucciones  
	if pc > len(instructions) {  
	    return 
	}  
	  
	// Obtener la instrucción actual en la posición del PC  
	return instructions[pc], nil
}
``` 