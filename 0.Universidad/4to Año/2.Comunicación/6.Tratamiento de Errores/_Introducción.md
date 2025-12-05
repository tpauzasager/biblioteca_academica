# Causa
- Ruido
- Atenuación 
- Distorsión 
- AB insuficiente
- T > C
- Pérdida de sincronismo
___
# Tipos de errores
Simples 
	- Afectan un solo bit 
	- Independientes entre si

Ráfaga
	- Afectan varios bits consecutivos
	- Independientes entre si

Agrupados
	- Tandas sucesivas de cierta duración 
	- Afectar varios bits no necesariamente seguidos
___
# Detección
Paridad
	Vertical -> Con cant de 1s de la secuencia
	Longitudinal -> Se cuenta un bit de cada secuencia
	Ciclicla -> Dos bits de paridad (cada uno chequea posicion par e impar de la ráfaga)

CRC
	- Se envía R(x)
	![[Pasted image 20251204203706.webp]]
CheckSum:
	![[Pasted image 20251204204024.webp]]
___
# Corrección 
ARQ (Corrección hacia atrás)
	- Control de flujo 
	- Pedir retransmisión 
	- Solo para Punto a Punto 
	Tipos
		- Stop & Wait: No puede volver a envías hasta que reciva respuesta de Rx (ACK, sin error, o NAK, con error)
		- Ventana Deslizante: Stop&Wait, pero con varios paquetes juntos (ventana) por cada ACK/NAK

FEC (Corrección hacia adelante)
	- Permite multipunto
	- Se envía el mismo paquete 2 veces
	- Si los dos tienen error => Pide retransmisión o se corrige por capa superior

Hamming (autocorrector)
	- Se agregan bits de paridad cada n bits del flujo (distancia de hamming) 
	- Estos permiten detección y corrección del paquete