# Definición de capas

| Nombre Capa  | Descripción                                                          | Funciones                                                                 | KeyWords                                 |
| ------------ | -------------------------------------------------------------------- | ------------------------------------------------------------------------- | ---------------------------------------- |
| Aplicación   | Interfaz de acceso al entorno OSI                                    |                                                                           |                                          |
| Presentación | Definición del formato de los datos                                  | - Encriptación                                                            |                                          |
| Sesión       | Gestión de sesiones entre aplicaciones                               | - Control de dialogo<br>- Recuperación de conexión interrumpida           |                                          |
| Transporte   | Mecanismo de intercambio de datos<br>Conexiones de extremo a extremo |                                                                           | - Orientación a **conexión** o **datos** |
| Red          | Direccionamiento lógico y enrrutamiento de paquetes                  |                                                                           | - IP dir                                 |
| Enlace       | Enlace confiable entre placas <br>Gestión de enlaces                 | - Control de flujo de b<br>- Detección/corrección/recuperación de errores | - MAC id<br>- Tramas                     |
| Físico       | Reglas para transmisión de bits                                      |                                                                           |                                          |

Cada capa entrega servicios a la capa superior, inferior y a su capa par (entre capas del mismo nivel) 

# Transporte
## Orientación
| Tipo     | Descripción                                                                                                    | Usos                |
| -------- | -------------------------------------------------------------------------------------------------------------- | ------------------- |
| Conexión | Establece conexión estable y se asegura que los datos lleguen como correctamente (hay corrección de errores)   | Web, mail           |
| Datos    | No se establece conexión, se envían datos directamente<br>No se garantiza orden ni calidad de datos entregados | Streaming<br>Juegos |