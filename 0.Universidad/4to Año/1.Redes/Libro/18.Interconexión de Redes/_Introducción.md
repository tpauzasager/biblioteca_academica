Capa 3 (red)
# Funciones Básicas

| Función                         | Descripción                                                                                              |
| ------------------------------- | -------------------------------------------------------------------------------------------------------- |
| Encapsulamiento                 | Datos transferidos en bloques (**PDU**)                                                                  |
| Fragmentación<br>y Reensamblado | Separar datos en paquetes más pequeños manejados por el protocolo y posterior reagrupación de los mismos |
| Control de conexión             | 1. Establecer conexión<br>2. Tranferencia de datos<br>3. Terminación de conexión                         |
| Entrega<br>Ordenada             |                                                                                                          |
| Control de flujo                | Limitar cantidad o tasa de datos enviada por el Rx                                                       |
| Control de erorres              |                                                                                                          |
| Direccionamiento                |                                                                                                          |
| Multiplexación                  | Multiples conexiones en el mismo canal                                                                   |
| Servicios de <br>transmisión    | - Prioridad<br>- Calidad de servicio<br>- Seguridad                                                      |

# Conexión 
Orientado a **conexión** 
	Ofrece
		- Retransmisión 
		- Enaminamiento 
		- **Garantiza entrega** 
		- Puede haber **corrección de errores** (por retransmisión)
	Limitaciones
		- Cada PDU va por el mismo camino 
Orientado a la **no conexión**
	Ofrece
		- **Velocidad** (pq puede ir por el camino de menor esfuerzo)
	Limitaciones
		- Cada PDU se trada independientemente 
		- Cada PDU puede ir por distintos caminos
