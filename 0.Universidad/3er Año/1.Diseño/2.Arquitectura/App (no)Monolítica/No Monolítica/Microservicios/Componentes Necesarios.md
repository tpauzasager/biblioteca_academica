| Nombre           | Descripción                                                                                                                                                                   |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Administración   | Responsable de colocación de servicios en nodos, identificación de errores, reequilibrio de servicios entre nodos, etc.                                                       |
| Service Registry | Mantiene **lista de servicios** y nodos en donde están. Para permitir la búsqueda.                                                                                            |
| API Gateway      | Es **punto de entrada para clientes**. Puede hacer balanceador de carga y IDM.<br>Todo cliente (ej: browser) va a parar acá y este reenvía llamada a los servicios apropiados |
