# Definición 
Se utiliza para la comunicación a través de redes interconectadas 

SA
	- Sistema Autónomo
	- Conjunto de routers y redes gestionados por una sola organización 
	- Poseen mismo protocolo de enrutamiento
___
# Protocolos
IRP (Interior)
- Para conumicación en el mismo **sistemas autónomos** (AS)
ERP (Exterior)
- Para comunicación entre diferentes AS
# Estrategia de ruteo
Vector distancia
	A - B - C       Vectores distancia:  router almacena el costo para enlace con redes coenctadas directamente
	 |    |     |   => {AB = 10; AE = 20} ; {BA = ... ; BF; BC}; {EA; EF} ; {FE; FB; FG}; ...
	E - F - G

Estado de enlace 
	- Todos los routers se conocen entre ellos 
	- Se envía intercambio de info de costo de enlace para todos los routers entre si 
	- Para IRP

Vector camino
	- Para ERP
	- No hay estimación para costo ni distancia 
	- Se busca saber cuales son los AS alcanzables desde el nodo actual
## Ejemplos
OSPF
	 - Tipo: **IRP** 
	 - Clasificación: **Estado Enlace**
	 - Encapsulamiento IP (pq tiene que ser rápido pq tiene que llegar a todos los router del AS)
	 - Calcula ruta de interconexión de redes por menor costo (usuario indica que es el costo)
	 - Router guarda BD con topología del AS
RIP
	- Tipo: **IRP** 
	- Clasificación: **Vector distancia** 
	- Encapsulamiento en UDP
	- 15 Saltos máx (si lo supera => ruta inalcanzable)
	- Puede ser usado por diferentes routers (no solo por un propietario)
BGP 
	- Tipo: ERP
	- Clasificación-> **Vector camino**
	- Encapsulamiento TCP 
	- Manda info de ruteo a todos los routers en el AS
	Funcionamiento
		1. Adquisición de routers vecinos (envio de mensaje TCP de aceptación o rechazo)
		2. Detección de vecino alcanzame 
		3. Detección de red alcanzable 
		Cada router mantiene BD con redes alcanzables y rutas preferidas 
		Al haber cambios, el router manda mensaje de actualización 