# Definición 
- Es lo que usa http para ser https
- Protocolo de seguridad p a p
	![[Pasted image 20251121082909.webp|600]]

Ventajas
	- Comunicación segura entre dos pares 
	- Estándar en la industria 
	- Confiabilidad 
	- Adopción (muchas erramientas soportan este protocolo)
Desventajas
	- Overhead 
	- Complejidad
	- Dependencias 
## Handshake
- Se establece configuración de la encriptación a utilizar 
- Se envía certificado público (avalado por entidad certificante) que atentica al servidor 
- Clave publica del certificante se usa para encriptar llave simetrica generada por el cliente (propia del cliente - servidor)

## MTLS
Mutial TLS (Mutua Confianza)
- Confianza mutua entre los pares 
- Mayor overhead en handshake
- Minima diferencia de overhead en comunicación 