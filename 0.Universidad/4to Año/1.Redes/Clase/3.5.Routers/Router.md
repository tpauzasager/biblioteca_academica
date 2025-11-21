# Router
- Dispositivo de capa 3 (OSI)
- Puertos para: LAN, WAN y consola
- Aprende direcciones IP
- Permite segmentación de la LAN (?)

# Ruteo 
Definición -> Encaminamiento de datagramas de una red a otra (mediante rutas)
Rutas 
	- Pueden ser estáticas o dinámicas (por protocolos de ruteo)
Protocolos
	- RIP, IGRP, OSPF, EGP
Tabla
	- Guarda la relación entre mascaras y el puerto al que deben entregar el datagrama
		- Puede ser por entrega directa o a un puerto en específico (en el caso de que necesite saltar a otro router)
## Protocolos de ruteo
IRP (Interior)
- Para conumicación en el mismo **sistemas autónomos** (AS) = Conjunto de redes que depende de un administrador determinado (ej: utn)
ERP (Exterior)
- Para comunicación entre diferentes sistemas autónomos 
## Estrategia de ruteo
### Clasificación
Vector distancia
	A - B - C       Vectores distancia:  router almacena el costo para enlace con redes coenctadas directamente
	 |    |     |   => {AB = 10; AE = 20} ; {BA = ... ; BF; BC}; {EA; EF} ; {FE; FB; FG}; ...
	E - F - G
	- Se usa para IRP	

Estado de enlace 
	- Todos los routers se conocen entre ellos 
	- Se envía intercambio de info de costo de enlace para todos los routers entre si 
	- Para IRP

Vector camino
	- Para ERP
	- No hay estimación para costo ni distancia 
	- Se busca saber cuales son los AS alcanzables desde el nodo actual
### Ejemplos
