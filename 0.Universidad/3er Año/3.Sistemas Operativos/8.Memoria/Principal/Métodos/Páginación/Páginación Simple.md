Definción:
	Los procesos están divididos en pequeñas páginas (de tamaño fijo)
	La memoria está dividida en frames (del mismo tamaño que las páginas)
	Cada proceso tiene una tabla de páginación (relaciona la pág con el marco en donde está)
	Cada pág tiene **bit de Validez**, indicando si está dentro del espacio de direcciones del proceso 

| Ventajas                                                                                                                                     | Desventajas                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| - Permite que dir físicas no sean contiguas<br>- Cualquier marco puede ser asignado a cualquier pág<br>- No genera **Framgentación Externa** | - Genera **Fragmentación Interna** en la útlima página |
___
# Pasaje DL -> DF
DL = Dir Lógica (decimal)
TM = Tamaño de pág
NM = Nro de Marco (en el que está el NP)
$$DL / TM = NP \space\space;\space\space resto = offse$$

$$DF = NM * TM + offset$$ ___
# Protección y Compartición
Protección:
	- Se agrega bits (rwx) en la TP que indique los permisos sobre las páginas

Memoria compartida:
	- Apuntando a los mismos marcos en distintos procesos

