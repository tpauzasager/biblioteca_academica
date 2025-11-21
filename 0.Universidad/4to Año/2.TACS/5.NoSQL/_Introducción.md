# Big Data
Definición:
	Datos que nacen del usuario al interactuar con el sistema 
___
# Métodos 
## Replicación 
### Activo-Pasivo
![[Pasted image 20251105161735.webp|300]]
Activo -> Lectura y escritura (y replica datos en el pasivo)
Pasivo -> Solo lectura 
Si se cae A => Activo la escritura en A'
Impacto
	Escritura -> bajo
	Lectura -> Alto
### Activo-Activo
![[Pasted image 20251105164757.webp|300]]
Gano disponibilidad 
Problema de concurrencia 

Métodos para solucionar concurrencia (conflictos)
	Consenso -> RAFT / Paxos
	Timestamp -> Guardo y chequeo el más nuevo 
	Quorum (W (nodos escritura) + R (nodos lectura) > N => Consistencia) -> Necesito N/2 +1 para dar respuesta válida 
## Particionamiento
Img sin la flecha que va de una a otra bd
![[Pasted image 20251105162018.webp|300]]
Se separan los datos a guardar (en función del negocio) y cada pedazo se almacena en bd diferentes

Impacto
	Escritura/Lectura -> depende de query (si solo pega a una bd => no cambia)
## Sharding
Dividir datos uniformemente dentro de n servidores 

Hash de distribución 
	-> Se le calcula hash a cada elemento y se lo guarda en un servidor en función de ese hash
Hash consistente 
	-> Hash tambien en función de la ip del usuario (y se le asigna un servidor al que conectarse) 
	-> Si C se cae => Todos los usuario que ubiesen ido a C, pasan a ir a B ![[Pasted image 20251105163548.webp|300]]
Hash consistente + Virtual nodes 
	-> Nodos virtuales representan a su respectivo Nodo real (ej: B1 == B), por eso se reparte mejor la carga, porque el tramo que cubre cada valor del hash es menor
	-> ![[Pasted image 20251105164232.webp|300]]
## Sharding + Replicación
![[Pasted image 20251105165355.webp|500]]
