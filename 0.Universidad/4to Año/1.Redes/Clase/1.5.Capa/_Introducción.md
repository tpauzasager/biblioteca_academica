Definición
	- Protocolo para resolución de direcciones (IP <-> MAC)
	- Existe dos (ARP y RARP)

# ARP
- Resolución de dir IP a MAC
Funcionamiento
	- Transmite broadcast MAC con dir IP (destino) y destinatario responde con su propia dir MAC
	- Respuesta se guarda en tabla ARP del host (pseudo cache)
# RARP
- Resolución MAC a IP
Funcionamiento
	- Transmite broadcast MAC a servidor RARP
	- Servidor RARP devuelve la dir IP correspondiente a la MAC
___
# Mensaje
- Mensaje ARP y RARP se encapsula en trama de capa 2 (pero no por eso es de capa 3)