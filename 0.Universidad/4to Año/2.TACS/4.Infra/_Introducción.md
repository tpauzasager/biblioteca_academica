# Definición 
Todo recurso de HW que da soporte a una aplicación
# Tradicional
Caracteristicas:
	- Performance 
	- Escalabilidad 
		- Horizontal -> Clustering 
		- Vertical -> Upgrade HW existente 
	- Disponibilidad 
		- Promedio de tiempo entre fallas
		- Promedio de tiempo en recuperarse
___
# Load Balancing
- Distribuir tráfico de red entre multiples servidores 
Tipos
	- Fisico
	- SW
Algoritmos
	- RR
	- IP Hash 
Stateful 
	Stickiness (mantiene servidor asignado)
	Centralized (Salto de red y SPOF) 
	Session Replication 
		- Los servidores se van pasando las modificaciones que hacen los usuarios en sus sesiones 
		Triggers
			- Genero la replicación cuando hay modificación en sesión (sesión sucia)
		Granularity
			- Nivel de gerarquia que se replica
			- Atributo, sesión o campo
___
# CDN
Content Delivery Network
Uso
	- Almacenar contenido estático (distribuido geograficamente)
	- Para que servidor no tenga que enviar contenido al user
___
# Fail over
Definición
	- Servidor falla => Se migra la conexión a otro servidor 
Transparent Failover
	- Cliente no se da cuenta de la caida del servidor
___
# Patterns para no Clustering
- Singleton 
- Abuscar del estado 
- Uso recursos remotos (sin cachear)