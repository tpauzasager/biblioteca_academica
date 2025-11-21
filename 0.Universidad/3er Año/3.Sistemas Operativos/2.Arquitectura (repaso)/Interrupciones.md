# Definición
Evento que lleva a un corte del flujo de ejecución normal de la CPU
**Siempre se ejecutan en modo KERNEL**, ya que, requieren acceso directo a recursos del sistema y es el SO quien las atiende (se carga el contexto de la rutina del SO correspondiente a la syscall)
# Clasificación

## Según Origen 
| Sincronas                                                  | Asíncronas                                              |
| ---------------------------------------------------------- | ------------------------------------------------------- |
| - Generada dentro de la CPU<br>- Resultado de la ejecución | - Independiente de la ejecución<br>- No son predecibles |
| Ej: División por cero                                      | Ej: Dispositivo externo envía interrupción a la CPU     |
## Según Prioridad
| Enmascarable                      | No Enmascarable       |
| --------------------------------- | --------------------- |
| Puede ser pospuesta por un tiempo | No puede ser ignorada |
|                                   |                       |


# Procesamiento
1. Controlador del dispositivo o HW externo genera una interrupción
2. Procesador completa ejecución de instrucción en curso
3. Procesador identifica fuente y la notifica
4. Procesador coloca PC y PSW en pila del sistema (guarda contexto)
5. Procesador carga el nuevo PC en función de la interrupción (que lo saca de la tabla guardada en memoria) 
- Se da el control al Interrupt Handler 
6. Se guarda el resto del estado de la CPU
7. Se procesa la interrupción
8. Se restaura contexto del CPU
9. Se restaura PC y PSW

