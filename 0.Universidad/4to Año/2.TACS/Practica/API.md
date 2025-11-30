1. Cuando usar SOAP sobre REST o GraphQL? Cuando usar gRPC?
	SOAP:
		- Más empresarial
		- Agnostico al paradigma y al protocolo de transporte 
		- Con el WSDL se tiene toda la documentación
		- Muy verboso y solo funciona con XML
		- Se le puede agregar la seguridad (pq es un protocolo)
	REST:
		- Simple y más usado
		- Solo sobre HTTP
		- Mecanismos incorporados de cacheo en el browser 
		- Si usas query params => No es cacheable (?)
	GraphQL:
		- Resuelve underfetchin (pedir menos de lo que me da), underfetching (pedir más de lo que me da) y N+1
		- Cada cliente pide exactamente lo que necesita (útil para recursos anidados)
		- Único endpoint => No afecta el agregar nuevos campos
	gRPC:
		- Alto rendimiento de velocidad y almacenamiento
		- Usa binary encoding 
		- Agnostico al lenguaje
2. Indique escenario hipotético en donde usar GraphQL. Que desventajas hay que tener en cuenta para evitar problemas futuros? 
3. Porque migraría de REST con JSON a gRPC con proto buffers 
4. Desventajas de API RESTfull.