
| Nombre                                    | Descripción                                                                                                                                              |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MutexCPU                                  | Hay un solo CPU => mutex                                                                                                                                 |
| PendingThreadsChannel                     | Buffer = 1 (el canal puede guardar un dato sin bloquearse, independientemente de si alguien lo recibió o no)<br>Se bloquea cuando recibe un 2do elemento |
| QuantumChannel                            | Se usa para informar finalización del Quantum                                                                                                            |
| MutexPlanificadorLP<br>WaitPlanificadorLP | Para el planificador a largo plazo                                                                                                                       |
