1. Itera por todas las particiones y las ocupadas las mete en otro slice 
2. Les modifica la Base y Limite a todas estas particiones ocupadas para que queden una al lado de la otra
3. Crea una única partición libre y la ingresa al final de la lista de particiones 
```go
func (d *Dinamicas) Compactar() {  
    logger.Debug("Entra a compactar")  
    var particionesOcupadas []memoriaTypes.Particion  
    espacioLibreTotal := 0  
  
    // Recorre las particiones, mueve las ocupadas al inicio y suma el tamaño de las libres  
    for _, particion := range d.Particiones {  
       if particion.Ocupado {  
          particionesOcupadas = append(particionesOcupadas, particion)  
       } else {  
          espacioLibreTotal += particion.Limite - particion.Base  
       }  
    }  
  
    // Calcula nuevas bases y límites para las particiones ocupadas  
    baseActual := 0  
    for i := range particionesOcupadas {  
		// Obtiene el tamaño de la partición
       tamano := particionesOcupadas[i].Limite - particionesOcupadas[i].Base  
		// Le da una nueva base y límite 
       particionesOcupadas[i].Base = baseActual  
       particionesOcupadas[i].Limite = baseActual + tamano  
       
       baseActual = particionesOcupadas[i].Limite  
    }  
  
    // Crea una partición libre con el espacio total restante  
    if espacioLibreTotal > 0 {  
       particionLibre := memoriaTypes.Particion{  
          Base:    baseActual,  
          Limite:  baseActual + espacioLibreTotal,  
          Ocupado: false,  
          Pid:     0,  
       }  
       particionesOcupadas = append(particionesOcupadas, particionLibre)  
    }  
  
    // Actualiza la lista de particiones  
    d.Particiones = particionesOcupadas  
    logger.Info("Compactación completada. Particiones actuales: %v", d.Particiones)  
}
```