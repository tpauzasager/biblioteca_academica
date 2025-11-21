# Tipos
| Nombre                | No Apropiativo                                                     | Apropiativo                                                                  |
| --------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| **otro nombre**       | - Sin desalojo<br>                                                 | - Con desalojo<br><br>                                                       |
| **Eventos atendidos** | - Solo tiene en cuenta eventos obligatorios (de liberación de CPU) | - Considera **al menos un** otro evento                                      |
| **Funcionamiento**    | - Esperan a que el proceso devuelva control al SO                  | - Puede interrumpir ejecución del proceso, para ejecutar uno más prioritario |

# Criterios 
según orientación 

| Usuario                                                                   | Sistema                                                                                           |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| - Tiempo de respuesta<br>- Predictibilidad<br>- Cumplimiento de deadlines | - Uso de CPU / recursos<br>- Throughput<br>- Tiempo espera / ejecución <br>- Respetar prioridades |

