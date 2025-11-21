1. Libera el espacio en memoria asignado al proceso 
```go
func FinishProcessHandler(w http.ResponseWriter, r *http.Request) {  
    // Leer el cuerpo de la solicitud (debe contener un JSON con la información del proceso)  
    var requestData types.RequestToMemory  
    err := json.NewDecoder(r.Body).Decode(&requestData)  
  
    // Extraer PID del cuerpo JSON enviado por ProcessToExit  
    pidS := requestData.Thread.PID  
    var errLiberar error  
    errLiberar = memoriaGlobals.SistemaParticiones.LiberarParticion(pidS)  
}
``` 