
Protocolo de Datagrama de Usuario

Definición:
	- PDU -> Datagrama UDP
	- (De)Multiplexado de puertos (direcciones)

Caracteristicas:
	- No confiable 
	- Sin validación 
	- Sin control de flujo 
	- Orientado a **no conexión** 
	- Gran **velocidad** 

Datagrama:
![[Pasted image 20250910150944.webp|600]]
	Caracteristicas:
		- Tamaño variable => Es necesario el cambpo de Longitud
		- Suma de verificación => Incluye: Trama UDP + ( Dir IP origen y destino + Cod de protocolo )   (por esto tiene doble detección de errores)
___
# QUIC
Quick UDP Internet Connections 
??????