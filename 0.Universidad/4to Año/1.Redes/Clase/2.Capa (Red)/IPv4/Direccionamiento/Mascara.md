# Clases
![[Pasted image 20250902104640.webp]]

dirección con todo 0 están reservadas
[rango de direcciones] -> Clase
[1;126] -> A
[128;191] -> B
[192;223] -> C
[124;239] -> D
[240;247] -> E
# Mascara Fija
Solo aplicable cuando uso IP con clase 

Definición 
	- Mecanismo para aprovechar mejor las grandes redes 
	- Se usan bits de dir host para subdividir la red 

Mascara 
	- 4B que indica 
	- Indica que parte de la dir IP se usa para host y que parte para red 
	- Se usa para poder interpretar la dir IP recibida 
	- '1' -> Red
	- '0' -> Host
	- ej: 255.255.000.000 => 2B para Red y 2B para Host
# Mascara Variable
VLSM 
- Permite uso más eficiente asignando diferentes máscaras a interfases de un router
# Sin Clase
CIDR
- Notación -> x.x.x/n      ;  n = cant de bits para red
- Ventajas:
	- No pierdo los primeros bits de la dir en identificar clase 