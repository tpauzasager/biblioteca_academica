# Definiciones
Puerto :
	- Ingreso a la red FR
	- Nacen los PVC (circuitos virtuales permanentes)
BC (bits) :
	- Cant más de bits por ráfaga transmitidos por pvc en un intervalo de tiempo
	- Con DE = '0'
TC (segundos) :
	- Intervalo de medición (con o sin actividad)
BE (bits) : 
	- Tamaña en exceso de ráfaga
	- Cantidad no comprometida (con DE seteado en '1') en TC

VP (bps) :
	- Velocidad del puerto 
	- Vel máxima de entrada a la red FR
	- $= (BC + BE)/TC = CIR + EIR$
CIR (bps) :
	- Velocidad de info comprometida 
	-  $=BC / TC$
EIR (bps) :
	- Vel de info en exceso 
	-  $=BE / TC$

![[Pasted image 20251017131558.webp]]
