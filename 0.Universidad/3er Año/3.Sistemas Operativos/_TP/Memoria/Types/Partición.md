```go
type Particion struct {  
	// Ambos expresados como posiciones aboslutas (tamaño se obtiene haciendo "Base - Limite") 
    Base    int  
    Limite  int  
	
    Ocupado bool  
    Pid     types.Pid  
}
````