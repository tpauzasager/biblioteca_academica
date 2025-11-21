# Definición 
![[Pasted image 20251112090243.webp|700]]
Objetivo:
	- Desacoplar aplicación del sistema de observabilidad 

# Señales 
Distributed Tracing
	- Poder tracear el flujo de una request a traves de todo el sistemas y los externos tambien 
	- Se le asigna un trace ID para poder construir el arbol del flujo 
	Usos
		- Buscar causa raíz 
		- Optimización 
		- Analisis de dependencias del sistema
	Instrumentación 
		- Automatica -> Java
		- Manual -> Python, Go, Node 
Metrics
Baggage
Logging
