Crea una única partición libre del tamaño total de la memoria, esta luego se irá acotando para dar lugar a nuevas particiones
```go
func (d *Dinamicas) Init() {  
    logger.Debug("******** Inicializando Particiones Dinámicas")  
    memSize := memoriaGlobals.Config.MemorySize  
    // d.Particiones = make([]memoriaTypes.Particion, memSize)  
    d.Particiones = append(d.Particiones, memoriaTypes.Particion{  
       Base:    0,  
       Limite:  memSize,  
       Ocupado: false,  
    })  
}
```
