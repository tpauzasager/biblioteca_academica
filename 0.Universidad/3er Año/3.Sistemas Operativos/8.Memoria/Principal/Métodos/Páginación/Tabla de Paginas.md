Definición:
	- Es una tabla fija con todos los números de pág de la memoria (representado por la posición en la tabla), el marco en el que está y el bit de validez (si pertenece o no a ese proceso) 
	- Está en **Memoria**, ya que no entre en los registros de la CPU (MMU)
	- No posee ni base ni límite
	- Solo tiene el nro de pág (multiplicandola por el tamaño de pág se obtiene la base y el límite es siempre el mismo)
	- **Cada proceso** tiene una tabla de página donde muestra que págs puede utilizar 

TLB
	- Cache que contiene la CPU 
	- Contiene una parte de la Tabla de páginas 
	- Primero busca en esta subtabla y luesgo (si ocurre un TLB miss) busca en la Tabla de págs 
___
# Jerarquica
![[Pasted image 20241025195649.png]]

Las tablas de pág de 2do nivel se crean a demanda 