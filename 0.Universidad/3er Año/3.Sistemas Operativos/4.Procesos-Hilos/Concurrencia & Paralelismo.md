![[Pasted image 20240830230308.png]]

# Cambio de Contexto
- Cuando se cambia el proceso de la CPU, se guarda su ***Contexto de Ejecución*** para poder reanudarlo
- Tiempo de overhead (2 por cada cambio de proceso)
## Objetivos
- Ejecutar otro proceso
- Atender una interrupción (ejecutar interrupt handler) 
- Ejecutar syscall
___
Afinidad de procesador -> Un proceso siempre ejecuta en mismo CPU
sin afinidad -> Única cola de planificación 
___
Cambio entre Hilos de mismo proceso -> Realizado por Usuario
Cambios entre Hilos de diferente proceso -> Realizado por SO (modo kernel) 