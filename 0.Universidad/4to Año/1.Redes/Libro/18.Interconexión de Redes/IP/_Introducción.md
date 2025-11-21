# Descripción 
Caracteristicas
	- Orientado a la **no conexión**
	- Robusto (pdu puede seguir muchos caminos)

Transporte:
	1. Capa 3 (con IP) recibe datos de capa superior y les agrega cabecera IP
	2. Datagrama se encapsula en protocolo LAN (LLC y MAC) y se envía por router
	3. Router recibe y lee cabecera IP y reenvía pdu
	4. Encapsulamiento para pasar por WAN 
	5. Llega al router destino y le quita campos WAN y reencapsula en LAN (otra diferente) con dir de B

Tipos de difusión:

| Nombre    | Tx  | Rx  | Subtipos                                                                                                           |
| --------- | --- | --- | ------------------------------------------------------------------------------------------------------------------ |
| Unicast   | 1   | 1   |                                                                                                                    |
| Broadcast | 1   | n   | Dirigido -> Limitada al broadcast de la red<br>Limitado -> A todos los host de la red local en la que está el disp |
| Multicast | 1   | m   | Pseudo patron observer                                                                                             |
# v4
![[Pasted image 20250921110959.webp]]
Desplazamiento del fragmento -> Indica posición del fragmento de datos dentro del datagrama original 
Protocolo -> UDP o TCP
## Clases
![[Pasted image 20250921111242.webp]]
Mascara
	'1' -> Indicador de red
	'0' -> Indicador de host
___
# v6
![[Pasted image 20250918155205.webp|500]]
## Dirección
Identifica Interfaz de Nodos
	Cada interfaz tiene varios nodos 
	Cada interfaz puede tener multiples dir asosciadas 
1ros 64b -> Clasificación / Agrupamiento  (permite rapidez)
2dos 64b -> Otros
## Tipos
Unidifusión (unicast) -> Identificador de una Interfaz 
Monodifusión (anycast) -> Identificador para conjunto de Interfaces (pero se entrega a solo una Interfaz, despues esta la distribuye como corresponde)
Multidifusión (multicast) -> Va directamente a todo el conjunto de interfaces 
## Link Local
Forma de dirección unicast
Para comunicación dentre de la red 
Contiene la dir MAC del dispositivo
Siempre empieza con FE80