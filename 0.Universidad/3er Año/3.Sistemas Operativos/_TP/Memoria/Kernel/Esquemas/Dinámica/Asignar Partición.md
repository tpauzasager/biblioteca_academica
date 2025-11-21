1. Obtiene la partición a asignar. Si no hay espacio suficiente (pero si libre separados), manda a compactar 
2. Si partición tiene tamaño exacto => La asigna y nada más 
3. Si partición tiene tamaño extra => Divide la partición en dos (una que será asignada al proceso y la otra para dejarla como libre)
   Luego se agregan estas particiones a la lista de particiones dinámicas 
```go
func (d *Dinamicas) AsignarProcesoAParticion(pid types.Pid, size int) (base uint32, err error) {  
    err, particionEncontrada := memoriaGlobals.EstrategiaAsignacion.BuscarParticion(size, &d.Particiones)  

	// Sino la estrategía no pudo asignar partición => Envía señar para compactar
    if err != nil {  
       if d.hayEspacioLibreSuficiente(size) {  
          return 0, errors.New(types.Compactacion)  
       } else {  
          return 0, err  
       }  
    }  
  
    tamParticion := particionEncontrada.Limite - particionEncontrada.Base  
    var nuevasParticiones []memoriaTypes.Particion  
  
    for i, particion := range d.Particiones {  
       if particion.Base == particionEncontrada.Base {  
          // Si a la particion encontrada le sobra espacio  
          
          // Chequeo si el tamanio de la particion es mayor a lo que el proceso requiere  
          if tamParticion > size { 
             nuevasParticiones = append(  
                nuevasParticiones, // vacia  
                memoriaTypes.Particion{ // Particion del proceso  
                   Base:    particionEncontrada.Base,  
                   Limite:  size + particionEncontrada.Base,  
                   Ocupado: true,  
                   Pid:     pid,  
                },  
                memoriaTypes.Particion{ //Particion de lo que sobro al asignar el proceso  
                   Base:    particionEncontrada.Base + size,  
                   Limite:  particionEncontrada.Base + tamParticion,  
                   Ocupado: false,  
                },  
             )  
             nuevasParticiones = append(nuevasParticiones, d.Particiones[i+1:]...)  
             d.Particiones = append(d.Particiones[:i], nuevasParticiones...)  
             // Si llega al else la particion encontrada tiene el justo tamaño del proceso asi que se le asgina y listo  
          } else if tamParticion == size {  
             particionEncontrada.Ocupado = true  
             particionEncontrada.Pid = pid  
          }  
          break  
       }  
    }  
    return uint32(particionEncontrada.Base), nil  
}
```