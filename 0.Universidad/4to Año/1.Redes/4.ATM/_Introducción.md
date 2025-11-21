
|       | Tolerante | No tolerante |
| ----- | --------- | ------------ |
| Voz   | Pérdida   | Retardo      |
| Datos | Retardo   | Pérdida      |
# Definición 
- Modo de Transferencia Asíncrónico 
- Sobre ISDN Banda ancha y SDH
- PDU -> Celda (o célula) con tamaño 53B
- Permite transmitir de todo (datos, voz, video)
- Tiene **capa de adaptación**
- Norma -> UIT (I.x.x.x) 

Asincrónico por
	- No está sincronizado respecto de ningún usuario
	- Asignación de recursos dinámica por demanda

Comportamiento
	- La nube casi no tiene procesamiento (se delega a las terminales)
	- Eso otorga mayor velocidad en Tx

PDU
	![[Pasted image 20251021113047.webp|600]]
	Header -> 5B
		- Info de enrutamiento
	Payload -> 48B
		- Puede llevar OYM (info de operación y mantenimiento)	

Canales
	VC 
		- Canal virtual con 1+ destino (Punto a Multipunto)
		- Identificador no único
	VP
		- Trayecto virtual (agrupación de VCs)	
		- Es el identificador de un conjunto de VCs que pertenecen al mismo cliente
		- Identificador único
___
# Arquitectura
![[Pasted image 20251021113811.webp|500]]
Planos de Operación 
	- Usuario -> Tx info de usuario y control de flujo y error
	- Control -> Control llamada y conexión
	- Gestión 
		- De Capa -> 
		- De Plano -> 
		
![[Pasted image 20251021114131.webp|500]]
Capas de ATM
	1. Física
		Convergencia Tx 
			- Independiza velocidad de flujo de celdas de interfaz física
			- Convierte flujo de celdar ATM en flujo de bits
			- Generación y chequeo de HEC (FRC para header)
	2. ATM 
		- Conmutación de celdas 
		- Armado de celdas (se agrega header)
		- Control de congestión y ruteo en UNI
	3. Adaptación de ATM
		- Segmentación y reenzamble -> Transforma PDU para poder ser transmitido por capa superior
![[Pasted image 20251116101554.webp|600]]
___
# Servicios
![[Pasted image 20251021120411.webp|700]]
## Capa de adaptación para cada servicio
![[Pasted image 20251021120919.webp|600]]
Clase A == AAL 1
Clase B == AAL 2
Clase C == AAL 3
Clase D == AAL 4
Existe un AAL 5
___
# Encabezamiento de Celda
![[Pasted image 20251021123134.webp|600]]

GFC -> Control de flujo
	- Solo está en UNI (pq el control de flujo ocurre ahí)
PT -> Tipo de carga útil 
CEP -> Prioridad de pérdida 
HEC -> Control de error de header (detección y aveces corrección simple) (CRC 8)