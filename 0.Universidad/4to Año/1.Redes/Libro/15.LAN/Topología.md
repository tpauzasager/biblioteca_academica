# Definición 
- Formato por el cual se interconectan entre sí las estaciones de la red

![[Pasted image 20250919102915.webp]]
Problemas
1. Es necesario indicar destinatario
2. Se necesita regular el acceso al medio (control de accesos)
PDU -> Trama
	- Datos
	- Info de control (contiene dir destino)
___
# Bus
- Todas conectadas en secuencia a traves de una misma canal 
- Multidireccional y full-duplex
- Cada señal transmitida hacia el canal es **recibida por todas las terminales** (pero solo el destinatario la copia)
- Hay **terminador** en cada extremo 
# Árbol 
- Generalización de BUS
- Medio de transmisión -> Cable ramificado sin bucles 
# Anillo 
- Terminales se conectan por repetidores que retrasmiten señal por el canal y copian trama (si son el receptor)
- Unidireccional 
- Hay un terminador en cada terminal
# Estrella 
- Cada estación conectada a central común a todas (dos canales: Tx y Rx)
Tipos:
	Difusión (hub) -> Retransmisión hacia todos los enlaces 
	Comnutador (switch) -> Almacenamiento temporal para determinar destinatario y retransmisión hacia destino (unicamemnte)

