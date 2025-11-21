![[Pasted image 20240830231216.png]]
[[0.Universidad/3er Año/3.Sistemas Operativos/999.Aclaraciones|Aclaración 3]]
En Espera:
- Proceso en cola de listos, pero no está en ejecución 
Bloqueado:
- No son planificables
___
# Planificadores
## Extra largo plazo
- Las realiza el administrador (espera un evento)
## <span style="color:rgb(255, 192, 0)">Largo plazo</span> 
- Controla grado de multi-programación 
## <span style="color:rgb(193,0,0)">Mediano plazo</span> 
- Controla suspensión de procesos
- Así controla uso de RAM
## <span style="color:rgb(0, 176, 240)">Corto plazo</span>
- Controla grado de multi-procesamiento 
- Es necesario que tenga el menor overhead posible 
## <span style="color:rgb(153, 153, 153)">Transiciones Grises</span>
- No son planificables, dependen de la ocurrencia de un evento 
___
# Swapping
- Los proceso bloqueados (En espera) pueden pasar al Disco para liberar la memoria a nuevas tareas
- Pasan a partición de 'Swap' del Disco
- Mayor aprovechamiento de RAM y CPU
- Mayor overhead
![[Pasted image 20240830233136.png]]


