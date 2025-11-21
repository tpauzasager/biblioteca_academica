1. Modifica los atributos de la partición para que se marque como libre 
2. Checkea que las particiones adyacentes este ocupadas
   Si no están => Fusiona dichas particiones (creando una nueva y volviendola a insertar)
   
```go
func (d *Dinamicas) LiberarParticion(pid types.Pid) error {  
    encontrada := false  
    for i := range d.Particiones {  
       particion := d.Particiones[i]  
  
       if particion.Pid == pid {  
          // Marcar la partición como libre  
          d.Particiones[i].Ocupado = false  
          d.Particiones[i].Pid = 0  
          encontrada = true  
  
          // Consolidación de particiones libres adyacentes  
          if i > 0 && !d.Particiones[i-1].Ocupado && i+1 < len(d.Particiones) && !d.Particiones[i+1].Ocupado {  
             // Caso 1: La partición actual y ambas adyacentes son libres  
             d.Particiones[i-1].Limite = d.Particiones[i+1].Limite  
             d.Particiones = append(d.Particiones[:i], d.Particiones[i+1:]...)  
  
          } else if i > 0 && !d.Particiones[i-1].Ocupado {  
             // Caso 2: La partición anterior es libre  
             d.Particiones[i-1].Limite = particion.Limite  
             d.Particiones = append(d.Particiones[:i], d.Particiones[i+1:]...)  
  
          } else if i+1 < len(d.Particiones) && !d.Particiones[i+1].Ocupado {  
             // Caso 3: La partición siguiente es libre  
             d.Particiones[i+1].Base = d.Particiones[i].Base  
             d.Particiones = append(d.Particiones[:i], d.Particiones[i+1:]...)  
          }  
          break  
       }  
    }  
    if !encontrada {  
       return fmt.Errorf("no se encontro particion que contenga el proceso PID: < %v >", pid)  
    }  
    return nil  
}
```