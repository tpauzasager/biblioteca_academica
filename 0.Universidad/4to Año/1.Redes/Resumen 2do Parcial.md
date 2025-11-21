![[Pasted image 20251117164152.webp|600]]
![[Pasted image 20251117164218.webp|600]]
___
# PPP
- Usos
	Establecer, configurar y probar conexión P2P (en capa 2 sobre enlaces seriales)
- Nace de HDLC
- Fases
	1. Establecimiento conexión 
		Se comunican los extremos por LCP para establecer config de la conexión
	2. Autenticación 
		No obligatorio
		Protocolos usados ->	PAP (no recomendado) o CHAP (recomendado)
	3. Configuración red 
		PPP puede llevar muchos protocolos a la vez 
		Protocolo usado ->		NCP
	4. Transmisión 
		LCP se usa para comprobar que linea sigue activa 
		PPP no cifra datos
	5. Terminación
- SLIP -> Peor y más vieja versión de PPP (solo permite IP)
- Ventajas
	Conexión por lineas sincronicas o asincronicas 
	Asignación dinámica de IPs (en ambos extremos)
	Transporte de varios prtocolos
	Implementa NCP (control de red)
	Se usa para implementar VPNs (si necesita cifrado => hay que hacerlo por debajo de PPP)
___
# HDLC
- Transparencia -> Bit stuffing 
___
# X.25:
 - Capas (OSI) -> 1, 2 y 3
 - Conmutación -> Capa 2 (circuito virtual permanente o temporal) o capa 3 (datagrama)
 - Componentes:
	 DTE -> Terminal de usuario 
	 DCE -> Router de acceso del usuario a la red del proveedor 
	 PAD -> Adaptador para DTEs asincronos (modo caracter) - Ensambla y desensambla los paquetes
- Planos la qu-> ?
	LAP-B ~= ABM (HDLC) => Full duplex ; Asincrono ; Cada terminal puede ser Primaria o Secundaria
- VC y LC
	VC (Virtual Chanel) -> Asociación lógica entre destino y origen (DTE - DTE) ; PVC (permanente) o SVC (temporal)
	LC (Logical Conection) -> Conmuta varios N2 en un N3 (DTE - DCE)
- Control errores
	Detección y retransmisión 
___
# Frame Relay:
- Capas (OSI) -> 1 y 2
- Conmutación 
	-> Capa 2 (circuito virtual permanente)
	-> DLC == PVC (circuito virtual permanente) | DLCI == Identificador de DLC
- Componentes:
	CTE -> Terminal de usuario
	POP -> Router de acceso del usuario a la red FR del proveedor 
	FRAD -> Adaptador para CTEs no compatibles con FR (de sincronico a sincronico)
- Ejercicio velocidades
	BE = Bits en exceso (con DE = 1)
	BC = Bits asegurados (DE = 0)
	CIR = BE / TC
	EIR = (BE + BC) / TC
- Planos -> Control y Usuario
	LAPD -> Control (gestión de conexión)
	LAPF -> Usuario (gestión datos de usuario)
		**-> Core => Sin control de flujo o error** (datos usuario)
		**-> Control => Con control de flujo y error** (control )
- Control congestión
	Prevención -> FENC (flujo) y BENC (congestión)
	Control -> Campo DE
- Control errores
	CRC-16 generado en CTE
	Detección y eliminación de tramas (sin corrección ni retransmisión)
	Solo en extremos
- ISDN -> Soportado por ISDN banda angosta
# ATM:
- PDU -> Celda (formada en capa ATM)
- Capas -> 3 (Fisica, ATM y AAL)
	OSI -> 1 y 2
- Conmutación 
	-> Capa 1 (OSI) == Capa 2 (ATM) 
	-> Conmutación física
- Componentes:
	UNI -> Protocolo entre usuario y proveedor ; Con control de flujo
	NNI -> Protocolo entre routers de proveedor ; No tiene control de flujo
- Canales -> Control (llamada y conexión), Usuario (datos de usuario) y Gestión (divido en gestión de capa y de plano)
- Control errores
	HEC -> Generado en cada extremo de ATM (solo sobre el header)
- ISDN -> Montado sobre ISDN banda ancha
- Orientado a la conexión
- Sincronismo
	Celdas envíadas por canal sincronico
	No está sincronizado con respecto a ningún usuario
	Posición de celdas en el flujo asignado en función a la demanda (no es fijo)
- Conmutación 
	VC (Virtual Channel) -> Circuito virtual de x.25 con multiples destinos ; VCI (identificador no unico)
	VP (Virtual Path) -> Asociación multiples VC que van a mismo destino ; VPI (identificador unico)
- Clases

|                      | 1   | 2   | 3   | 4   |
| -------------------- | --- | --- | --- | --- |
| Orientado a Conexión | x   | x   | x   |     |
| Sensible a retraso   | x   | x   |     |     |
| Bit rate fijo        | x   |     |     |     |
___
# MPLS:
___
# DNS: 
- Para convertir IP <-> nombre dominio 
- Usa UDP (sin conexión) y TCP (con conexión)