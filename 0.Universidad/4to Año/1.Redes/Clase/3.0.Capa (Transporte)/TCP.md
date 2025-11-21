Protocolo de Control de Transmisión 

Definición:
	 - Mensajes ACK / NAK (ARQ)
	 - Usa IP
	 - PDU -> Segmento TCP
	 - Usa puertos para (De)Multiplexar

Caracteristicas:
	 - Full Duplex
	- Orientado a conexión 
	- Control de flujo (Tx/Rx) -> Venta deslizante (ARQ) Ventana variable
	- Control de congestión (Tx/Red) ->

Segmento TCP:
![[Pasted image 20250910153728.webp|600]]
Checksum -> (igual que en UDP) Incluye Dir ip Origen y Destino 


# Congestión 
- Retraso severo por sobrecarga de datagramas en uno/s puntos de comuntación 
- Produce colapso
- Evitarlo por
	- Algorítmos 
	- Tecnicas de
		- Disminución multiplicativa (Correctivo) 
		- Arranque lengo (Preventivo)