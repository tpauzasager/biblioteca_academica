	# HDLC
High-level Data Link Control 

Caracteristicas
	- Sincróico 
	- Orientado al bit
	- ARQ ventana deslizante 

PDU -> Trama
![[Pasted image 20251014123955.webp|600]]
B -> Bandera (para sincronismo)
D -> Dirección 
C -> Control
FCS -> CRC(16) 
Tam max == 135B
## Control
8 bits
![[Pasted image 20251014125205.webp|600]]
16 bits:
![[Pasted image 20251014125225.webp|600]]

## Configuraciones
Jerarquico 
	- Puede ser o no jerárquico (con estación primaria o secundaria)
	- Tipo de mensaje (desde -> hasta)
		Primaria -> Secuendaria => Orden/Comando
		Secundaria -> Primaria => Respuesta
	- Balanceo
		- Balanceado (Estaciones pueden pasar de secundaria <-> primaria; según la comunicación) == P2P
		- No balanceado (una Primaria y el resto secundarias)
## Modos Respuesta
Respuesta Normal (**NRM**)
	- No balanceado, P2P o Multipunto, Half-Duplex
	- Transmisión cuando permite primaria
Asíncrona (**ARM**)
	- No balanceado, P2P, Full-Duplex
	- Transmisión sin permiso de primaria
Balanceado Asíncrono (**ABM**)
	- Cada estación es primaria y secundaria 
	- Enlace P2P, Full-Dulpex
## Tipos de Tramas
Depende de campo Control de la trama
No numeradas (U) 
	- Conexión y Desconexión 
	- No llevan nro de secuencia
Información (I)
	- Tiene nro de secuencia
Supervisión (S)
	- Control dea errores y flujo 
	- Tiene nro de secuencia
## Delimitación 
- Linea inactiva = `01111111`
- Bandera = `01111110`
## Transparencia
Para evitar secuencia de datos similar a las banderas (así no se interpreta como bandera y Rx lee bien la secuencia de datos)
Funcionamiento
	- bit Stuffing: `11111` -> Inserta 0 en Tx
	- `111110` -> Elimina el 0 en Rx
## Dirección 
- Único para cada secundaria 
- De grupo (enlace Multipunto - NRM)
- De difusión (enlace Multipunto - NRM)
## BIT P/F
pseudo RTS/CTS
- 1 y Orden => Primaria pide confirmación 
- 1 y Respuesta => Confirmación de RX