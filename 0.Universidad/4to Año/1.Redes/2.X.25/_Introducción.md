# Definición
Definición
	- Conjunto de protocolos
	- Enlaces poco confiables (gran BER)
	- Interfaz usuario/red (DTE/DCE)
	- Comprende las capas: 1, 2 y 3 (de OSI)
	- Orientado a conexión (Circuito virtual)
	- Conmutación en la capa 3

![[Pasted image 20251014122617.webp]]

DCE -> Proveedor
DTE -> Cliente

MOD 
	1ro. Cliente
	2do. Proveedor 
	3ro. PSE
___
# PDUs 
![[Pasted image 20251014123020.webp|600]]

Control de errores == Detección (solo)
___
# Niveles
## Fisico 
Define
	- Caract mecánicas, electricas, funcionales y procedurales para conexión física entre DTE y DCE
Tipos

| Versión  | Enlace    | Conector | Señal         |
| -------- | --------- | -------- | ------------- |
| X.21     | Digital   | DB-15    | Balanceado    |
| X.21 BIS | Analógico | DB-25    | Desbalanceado |
Caracteristicas
	- $V_{Tx,Max} = 64Kbps$
## Enlace
- Para tener enlace libre de errores 
- PDU -> Trama
- Protocolo -> HDLC (LAP-B == ABM) 
	- Balanceado (asincrónico) => P2P (solo dos usuarios)
	- Full-Duplex
	- ARQ ventana deslizante
	- Confirmación superpuesta mediante **piggyback** 
		- Mientras transmito, voy confirmando lo que recibí 
## Red 
- Conmutación 
	- Datagrama
		- Ocurre en capa 3
		- Cada uno posee un identificador 
	- Circuitos virtuales
		- Ocurre en capa 2
		- Asociación lógica de multiples canales entre origen y destino 
		- Significado extremo a extremo (DTE/DTE) 
		- Puede ser: PVC (permanentes) o SVC (no permanentes)

Paquete:
![[Pasted image 20251014175351.webp]]

GFI -> Formato gral del paquete (8 o 128)
LCI -> Canales logícos (o a 4095)
TPI -> Tipo de paquete ()
Para paquetes de llamada:
ADD -> Campo de dirección 
FAC -> Campo de facilidades 
	- Cobro revertido 
	- Grupo cerrado 
	- Selección rápida 
	- Negociación tamaño de ventana/paquete/clase de tráfico
Datos de usuario de llamada (opcional) -> Identifica protocolo superior
___
# Modos de Operación 
Paquete 
	- Sincronico
	- Canal lógico en cada enlace 
Caracter
	- Sincronico hasta el PAD (parte azul) -> Sin jerarquia
	- Asincronico (parte verde) -> Se agrega caracter de arranque y parada en el pdu
	- Permite integrar algo asincronico en un sistema sincronico
	![[Pasted image 20251014180803.webp|600]] PAD = Desemsamblador / Ensamblador de paquetes

