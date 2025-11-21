# Definición 
- Tiene capa 1 y capa 2 (cuadro)
- Conmutación rápida de paquetes (en capa 2)
- Menor BER (que x.25)
- Se usa para reemplazar lineas P2P
- Retransmisión se genera por estaciones terminales 
- No hay corrección ni retransmisión en FR (pero si puede haber en las LANs que conecta)

Caracteristicas
	- Circuitos virtuales (VC) de nivel 2 permanentes (PVC)
	- Reemplaza canal lógico (del x.25) por DLCI (Data Link Connection Identifier)
	- VC == Asociación lógica de varios DLCIs 
	- Conmutación a nivel cuadro
	- Uso dinámico de AB (en función de la info a transmitir)
	- Orientado a tráfico de ráfaga (tipo LAN)
	- Sobre ISDN banda angosta :
		- Contiene canl B (info usuario) y D (datos de red)

Dispositivos:
	CPE :
		- Enrutadores extremos del P2P (de los clientes)
		- Forma la LAN (las que se conectar a travez de FR)
		- FRAD (Dispositivo de acceso a FR) == Enrutador para FR (reemplaza al PAD del x.25)
	POP : 
		- Conmutadores rápidos (conforman la nube y los DLCIs)
		- Dan acceeso a la red FR

Nivel 2:
	- LAPD y LAPF (HDLC con pdu = cuadro) :
		- LAPD -> Canal D (datos de red) 
		- LAPF -> Canales B (datos de usuario)
			- Core (o central) -> Maneja info salto por salto
			- Control -> Meneja info de P2P
___
# Arquitectura
Planos de operación
	- Control 
		- Control de errores y de flujo
		- Establecimiento, liberación de conexiones lógicas  
		- Entre Usuario y Red
	- Usuario 
		- Transferencia de datos de usuario (extremo a extremo)
		- Tambien se toman acciones para que funcione bien la red
![[Pasted image 20251015195503.webp|600]]
Norma I.430/I.431 -> ISDN
![[Pasted image 20251017124411.webp|600]]

Datos == LAPF (control + core)
	- Control -> Extremo a Extremo
	- Core -> Salto por Salto 
Canal D == LAPD -> Salto por Salto (para **señalización**)
___
# PDU
PDU -> Cuadros
LAPD: ![[Pasted image 20251017124557.webp|600]]
LAPF: ![[Pasted image 20251017124620.webp|600]]
Dirección (LAPF core) :  ![[Pasted image 20251017124725.webp|600]]
DLCI -> Puede extenderse de 10b a 16b o 32b
C/R -> Orden o Respuesta
EA0 -> Siempre en '0'
F y B :
	- Notificación de congestión F (para adelante) y B (para atras)
	- Seteado por POPs
DE -> Si están en '1' => Se eliminan al detectar congestión 
EA1 -> Siempre en '1'
___
# Control de Errores y Congestión
Control de extremo a extremo
Retransmisión en cada nodo
Capa superior corrige 

Control :
	- Solo detección (FCS)
	- Corrección se hace en capa superior
	- **LAPF contro**l lleva secuenciamiento de cuadros 
Prevención congestión :
	- **LAPF core** previene congestión por bits:
		- F y B (seteados por los POPs)
		- Estos bits los detectan los CPE
Control de congestión :
	- Si en '1' => Se descarta el cuadro si hay congestión
Control de flujo :
	- Se hace de extremo a extremo 
	- Por el **LAPF control**
## FECN y BECN
estudiar mejor está parte que no la entendí bien
![[Pasted image 20251017130459.webp|600]]
R1 y R2 == CPE 
FRS == POP
___
# Sobresuscripción 
Definición 
	- Asignación dinámica del AB a los PVCs 
	- Multiplexado estadístico
	- $\sum CIR_i > VP$
___
# Voz sobre FR
Voz sobre IP
	- En capa 3
	- Comnutación de paquetes
Caracteristicas
	- Voz es tolerante a perdidas y no a retardos (=> pocos saltos para evitar retardo)
	- Menor QoS y costo (frente a telefonía común)
	- No acepta retransmición 
	- Aprovecha silencios 
	- Hay algoritmos de compreción (PCM)
Funcionamiento
	- Prioriza tráfico (usa DLCI específicos para voz)
	- Menor tamaño de cuadros (fragmentación)
	- Frads (o routers) para voz y datos	
Ventaja
	- Más confiable (pq está orientado a la conexión)
	- Menor procesamiento para comunicaciones entre FR (si es por VoIP => Requiere encapsular y desencapsultar)
Desventaja
	- IP se puede encapsular en cualquier protocolo de capa 2, pero VoFR no (porque ya es de capa 2)