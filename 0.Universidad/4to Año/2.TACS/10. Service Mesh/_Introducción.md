# Definición 
Service Registry
	- Cuando yo tengo varias instancias dinamicas de los servicios, se encarga de Indicarle a los consumidores que instancias están disponibles para consumir
	- Ejecuta Health-check (SR -> Servicio)
	- Escucha HeartBeat (cada servicio envía al SR una señal para que sepa que está escuchando) (Servicio -> SR)
	Como se registran nuevas instancias
		- Self Registry -> Cada instancia es responsable de avisar 
		- 3rd Party -> Coordinador extrenos se encarga de avisar 

Egress Mesh -> Para comunicación por fuera de la mesh de servicios propios

# Soluciones

| Server Side                                | Client Side                                    | Sidecar                                    |
| ------------------------------------------ | ---------------------------------------------- | ------------------------------------------ |
| ![[Pasted image 20251121092433.webp\|300]] | ![[Pasted image 20251121093018.webp\|200]]<br> | ![[Pasted image 20251121111623.webp\|400]] |
Server Side
	Load Balancer
		- Hace el routing a distintas instancias de B
	Desventajas
		1. SPF en LB

Client Side
	- Consulta al SR para saber las instancias disponibles
	Desventajas
		- Mayor acoplamiento
		- Necesito una forma confiable de avisarle a A las instancias disponibles
	Métodos de Implementación 
		Ad Hoc
			- Cada servicio implementa un método de routing diferente 
			- Poco eficinete y mucha repetición de trabajo (más propenso a errores)
		Biblioteca
			- Lockeo de lenguaje/FrameWork/Paradigma
			- Problema en la lib tira toda la app

Sidecar Proxy
	- Se mueve logica de red a un proxy propio del servicio 
	- Cada instancia habla con el Sidecar proxy propio (para entrada y salida)
	Ventajas
		- Intermedio y escalable. 
		- Es código de arquitectura (pq no depende del modelo => más desacoplado)
		- No hay spf (si se rompe un sidecar, solo afecta a ese servicio)
		- Cada sidecar puede ser desarrollado en stack tec diferente (pq se comunica por http)
		- Gobierno total (puede implementar los cambios que quiera pq no afecta a nadie)
	Desventajas
		- Mayor complejidad 
		- Otro punto más donde fallar 
	Control Plane
		- Maneja los Sidecar
		- Indica las instancias accesibles de los sidecars
		- SPF (para la modificación de instancias, pero los sidecar pueden seguir funcionando si las instancias se mantienen)
		- No requiere 100% HV
		- Facil de implementar cambios que afecten a todos los servicios
		Funcionalidades
			- Routing, Balanceo, Health Check
			- Monitoreo
			- Seguridad -> Acceso, Encriptación 
			- Reintentos / Time outs
			- Manejo desbordes -> Circuit Braker, Rate Limit
			- Caching
	