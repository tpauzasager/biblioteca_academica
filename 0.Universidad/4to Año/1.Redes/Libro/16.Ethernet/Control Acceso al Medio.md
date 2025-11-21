 $T_p$ = Tiempo de propagación = Tiempo que tarda el PDU en llegar del origen al destino (relacionado con dist entre estaciones)
 $T_{Tx}$ = Tiempo de transmisión = Tiempo que tarda en enviar (ponerlo en el canal) el PDU (relacionado con tamaño de PDU)

 $RTT$ = Round Trip Time = $2·T_p$ = Ida y vuelte entre estaciones
$RTT_{max}$ = Ventana de colisión = $RTT$ entre disp más lejanos 

Prob de colisión:
	$\propto^{-1} T_{Tx}$   ; Pero genera bloqueo del canal => no puede ser muy grande
	$\propto T_p$ 
___
# Contienda
**Aleatorios**
Aloha
	- No sensa ocupación de canal 
	- Manda y detecta colision 
	- Si hay colisión => Retransmito
	- Tipos:
		- Puro -> Sin restricciones
		- Ranurado -> Transmision ocurre en ranuras de tiempo determinadas (menor prob de colisión y requiere sincro)

CSMA (acceso multiple por sensado de portadora)
	- Sensa presencia de protadora en canal 
	- No ocupado => Toma el canal
	- Ocupado =>
		- P-Persistente [P=prob]-> Espera $RTT_{max}*P$ para sensar de nuevo
		- No persistente -> Sensa cada un tiempo aleatorio

CSMA/CA (evitar colisiones) IEEE 802.11
	- Sensado permanente 
	- Varias tecnicas para evitar colisiones

CSMA/CD (detección colisiones) IEEE 802.3
	- Además detecta colisiones y las resulve 
	- Sensado permanente y transmite ni bien puede
	- Aborta transmisión cuando hay colisión 
	- Espera t aleatorio para reintentar
## CSMA/CD
Formula de elección de ranura:
	$n=[0;(2^i -1)]$  / $i$ = cant de colisiones hasta el momento
	Ranuera de espera = $51,2 \mu s$ a 10Mbps = Tiempo de transmision de trama ethernet mínima (64B)  
10 colisiones -> Se deja de aumentar cant de ranuras
16 colisiones -> Capa MAC aborta transmision
___
# Token Passing
**Deterministico**
Token Ring (IEEE 802.5)
	- Elimina prob de colisión
	- Solo puede transmitir dispositivo que tiene el token 
	- Monopolización de canal
	- FDDI -> Doble anillo
![[Pasted image 20250826100851.webp]]Token Bus (IEEE 802.4)
	- Se define un anillo lógico por el que se gestiona el token
