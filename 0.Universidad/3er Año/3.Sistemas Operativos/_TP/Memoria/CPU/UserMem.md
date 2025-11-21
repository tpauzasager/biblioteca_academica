# ReadMemory
```go
	// Obtiene parametros por query param
	dirS := query.Get("addr")  
	tidS := query.Get("tid")  
	pidS := query.Get("pid")  
	  
	// Obtiene los 4B de la memoria de usuario
	cautroMordidas, err := helpers.ReadMemory(dir)  
	// Lo pasa a binario en BigEndiand y lo devuelve por http 
	data := binary.BigEndian.Uint32(cautroMordidas[:])
```
___
# WriteMemory
```go
	// Obtiene Thread y dirección por query params
	dirS := query.Get("addr")  
	tidS := query.Get("tid")  
	pidS := query.Get("pid")

	// Obtiene los 4B pasados por body
	var data uint32  
	err = json.Unmarshal(body, &data)  
	  
	// Guarda los datos recibidos del body en variable cuatromorididas
	var cuatromordidas = make([]byte, 4)  
	binary.BigEndian.PutUint32(cuatromordidas, data)

	// Escribe los 4B en la memoria de usuario
	err = helpers.WriteMemory(dir, cuatromordidas)
```
### helpers.WriteMemory
```go
func WriteMemory(dir int, data []byte) error {  

	// Valida que la dirección 
    if !ValidMemAddress(dir) {  
       err := errors.New("no existe la dirección física solicitada")  
       return err  
    }  

	// Escribe los 4B en la memoria
    for i := 0; i <= 3; i++ {  
       memoriaGlobals.UserMem[dir+i] = data[i]  
    }  
    return nil  
}
```