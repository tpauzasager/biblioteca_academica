Caracteristicas
	- Servicios se comunican por Web Service

Manejo Errores y desbordes
	- Hace falta un Circuit Braker (para cuando servicio se rompe, corta flujo para que no siga llamando a otros servicios continuando con el error)
	- Time outs entre cajas 
		- Reintentos para endpionts idempotentes

Problemas
	- Responsabilidad cruzada
	- Overhead (por pasamanos de request)
	- Redundancia de tareas 
	- Mayor complejidad (en desarrollo y gestión)
	- No hacer servicios muy pequeños 
	- Zona segura ahora incluye a varios servicios

Requisitos
	- Ser elastico (escalabilidad muy dinámica)
	- Conocimiento técnico en la empresa 

Malas prácticas
	- Mismo repo para varios servicios
	- Elegir SDKs sobre APIs
	- Ambiente compartido entre servicios
	- Mensajería sin versionado ni retrocompatibilidad
	- Servicios _olvidados_

Monitoreo y Observabilidad
	- Trace de la request más complicado 
	- Cada vulnerabilidad afecta a varios equipos

Ciclo de Vida
	- Es necesario que sean diferentes ciclos de vida entre servicios (para que varios equipos trabajen en parelelo)

Testing
	- Ambiente BETA con datos de prueba, pero ambiente estable

Disponibilidad 
	- Servicios criticos tienen que tener alta disponibilidad 
	- Necesito estar preparado para si un servicio se cae