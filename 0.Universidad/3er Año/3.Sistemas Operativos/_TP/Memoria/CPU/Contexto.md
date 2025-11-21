# GetContext
```go
	query := r.URL.Query()  
	// Recibe Thread por query param
	tidS := query.Get("tid")  
	pidS := query.Get("pid")  

	// Crea un dato tipo Thread para poder usarlo en el map
	thread := types.Thread{PID: types.Pid(pid), TID: types.Tid(tid)}  
	// Obtiene el contexto del Thread  
	context, exists := memoriaGlobals.ExecContext[thread]
```
___
# SaveContext
```go
	// Obtiene Thread por queryparam
	tidS := queryParams.Get("tid")  
	pidS := queryParams.Get("pid")

	// Obtiene y hace decode del contexto obtenido por body
	body, err := io.ReadAll(r.Body)  
	defer r.Body.Close()  
	  
	var contexto types.ExecutionContext  
	err = json.Unmarshal(body, &contexto)  

	// Lockea el mutex antes de guardar el contexto 
	memoriaGlobals.MutexContext.Lock()  
	memoriaGlobals.ExecContext[thread] = contexto  
	memoriaGlobals.MutexContext.Unlock()
```