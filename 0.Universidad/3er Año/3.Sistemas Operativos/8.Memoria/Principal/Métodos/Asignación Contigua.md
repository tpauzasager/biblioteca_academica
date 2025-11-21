![[Pasted image 20241025170411.png]]
Cada proceso cuenta con una Base y Limite para establecer su espacio de memoria asignado
___
## Particiones Dinámicas
- El tamaño de la partición del proceso se define en el momento de carga

| Ventajas                                                                            | Desventajas                     |
| ----------------------------------------------------------------------------------- | ------------------------------- |
| - No se limita la cant de procesos en memoria<br>- No hay **Fragmentación Interna** | - Hay **Fragmentación Externa** |
### Algoritmos de asignación de partición
| Nombre Algo      | Descripción                               |
| ---------------- | ----------------------------------------- |
| Primer ajuste    | El 1er hueco en el que entre              |
| Siguiente ajuste | El 1ro partiendo desde la última búsqueda |
| Mejor ajuste     | El más peuqeño en el que entre            |
| Peor ajuste      | El más grande en el que entre             |
___
## Particiones Fijas
- La memoria está dividida en N particiones pre-definidas de tamaño fijo

| Ventajas                                                                                                                                      | Desventajas                                                                                                                                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| - Cualquier partición liberada puede ser usada por cualquier otro proceso<br>- No hay **Fragmentación Externa**<br>- Más fácil de administrar | - Un proceso no puede ser más grande que el tamaño de las particiones<br>- No pueden haber más de N procesos en memoria<br>- Genera **Fragmentación Interna**<br>- Dificultad para compartir espacio entre procesos (se comparte todo o nada)<br> |
