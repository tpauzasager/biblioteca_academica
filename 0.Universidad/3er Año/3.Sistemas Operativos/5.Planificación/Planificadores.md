![[Pasted image 20240830231216.png]]
___

| Tipo Planificador                                       | Determina                                                                                                                                                                                               | Controla                     |
| ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| <span style="color:rgb(255, 192, 0)">Largo Plazo</span> | - Al cerrarse un proceso, decide cuando activar uno nuevo<br>- En función de su prioridad del job:<br>    - Prioridad<br>    - Balance CPU bound y IO bound<br>    - Optimizar performance              | - Grado de multiprogramación |
| <span style="color:rgb(192, 0, 0)">Mediano Plazo</span> | - Cuando y realiza operaciones de **swapping**<br>- Si es necesario suspender un proceso                                                                                                                | - Grado de multiprogramación |
| <span style="color:rgb(0, 176, 240)">Corto Plazo</span> | - Invocado cuando evento que libera CPU o posibilidad de reemplazarlo por mayor prioridad<br>- Que proceso (en ready) pasa a ejecutarse<br>- Se ejecuta muchas veces ==> Buena política y poco overhead | -                            |
___
# Prioridades
- Cada proceso tiene asociado un número entero 
- Menor número == Mayor prioridad 

- Starvation: Procesos de baja prioridad pueden no ejecutarse nunca 
- Aging: Cuanto más pasa el tiempo sin ser ejecutada => Aumenta su prioridad 