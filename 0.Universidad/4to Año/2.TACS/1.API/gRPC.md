Google - Remote Procedure Calls

Caracteristicas
	- Framework: RPC
	- Usa protocol buffers
	**- Load balancing del lado del cliente** 
	- Tracing
	- Health checking 
	- Autenticación 
	**- Full duplex** (http2)
	- Cascading call-cancellation (?)
	- Flow-control en capa de aplicación 
	- Payload agnostic (puede usar otro tipo de serialización)
	- Propio manejo de errores

Usos
	- Sistemas internos
	- Comunicación entre servicios cloud (pq tiene load balancing en cliente)

___
# HTTP2
![[Pasted image 20250903202626.webp]]