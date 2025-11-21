# CAP
Consistencia
- No tener lectura fantasma
- Cada lectura recibe el estado más actualizado (o un error)
Disponibilidad
- Cada request (R o W) recibe respuesta (sin importar si es o no el más actualizado)
Tolerancia a Particiones 
- Sistema continúa funcionando aunque hayan problemas de red
___
# ACID
Atomicidad -> Cada transacción se completo al 100% o 0% 
Consistencia -> Cada transacción lleva de estado consistente a otro
Isolation -> Transacción no afecta a otra en paralelo (que no se commiteo)
Duración -> Que no se borren los datos 
___
# BASE
Basic Availability -> BD disponible la mayoría del tiempo
Soft-State -> BD puede cambia incluso sin entrada (por ej: por procesos automáticos para garantizar consistencia con otros nodos)
Eventual Consisten -> Eventualmente los datos son los mimos en todos los servidores 
