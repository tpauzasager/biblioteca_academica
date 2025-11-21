# Wireshark
CAPA 2:

____
# Selección de Trama
A :
	-> Último digito 
	-> Para captura de capa 2 y 3
B :
	-> Digito verificador
	-> Para captura de capa 4
# Capa 2
1. MAC add
	Destino y origen
	Se pone en hexa
2. Tipo cast
	Unicast -> Otros
	Multicast -> Red = '1110...'
	Broadcast -> Host = FF...
3. Tipo trama 802.3
	- En campo Tipo/Longitud
	- LEN = < 1500 (#05DC)
		- Indica longitud del campo dato
	- Ethernetype = > 1536 (#0600)
		- Se agrega el protocolo que encapsula
		- Indica el protocolo que encapsulo (es trama Ethernet II)
			- #0800 -> IP4
			- \#86DD -> IP6
			- \#0806 -> ARP
4. Nro Vlan
	Para tramas 802.1Q: 
	![[Pasted image 20251026085424.webp|550]]
	- Puede ser la default ('1'), ahí no hoy vlan tag en la trama 
5. Protocolo encapsulado (CAPA 3)
# Capa 3
1. IP add
	- Destino y Origen (en decimal)
2. Protocolo encapsulado -> (de la capa superior)
3. Tipo PDU 
	- Única  - Fragmento Intermedio  - Fragmento Último 
	- Se indica en campo FLAG de trama
# Capa 4
1. Puerto 
	Origen y destino 
2. Protocolo encapsulado (de capa 5)
	- Se sabe por el puerto