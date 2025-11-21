# Programada
![[Pasted image 20240828162403.png]]
# Basada en Interrupciones
![[Pasted image 20240828162422.png]]
# Direct Memory Access
![[Pasted image 20240828162438.png]]
1. Se le pasa la información necesario al DMA, para que luego el lea y escriba los datos en la memoria, luego la CPU continua con su ejecución normal.
2. Luego, por una interrupción, la CPU lee la información leída y continua con ejecución.

| Ventajas                                                         | Desventajas                                                 |
| ---------------------------------------------------------------- | ----------------------------------------------------------- |
| Se libera CPU (solo interviene en inicio y fin de transferencia) | Requiere un HW especial                                     |
| Transferencias mucho más eficientes (en mayoría de casos)        | Requiere más tiempo inicial de set up del pedido (overhead) |
|                                                                  | Robo de ciclo de bus                                        |