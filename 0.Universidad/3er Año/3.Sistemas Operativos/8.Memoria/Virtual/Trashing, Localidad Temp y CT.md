Definición:
	Cuando un proceso no tiene la cantidad de frames necesarios para poder funcionar 
	Proceso queda realizando acciones de paginación sin realizar trabajo productivo

![[Pasted image 20241026185142.png]]

Solución:
![[Pasted image 20241026185202.png]]
Cant de frames totales o asignados a cada proceso. El resultado no cambia, pero se usa uno u otro en función del análisis
___
# Localidad Temporal
Definición:
	Conjunto de páginas a las que un proceso accede activamente y que necesita para poder funcioanr correctamente
___
# Conjunto de Trabajo
Definición:
	Estimación de la Localidad Temporal (usando las utlimas N pág referenciadas)
	En función de esto, se calcula la cant de frames que tiene que tener disponible para poder funcionar

 Asignación Dinámica:
	 $\sum{CT_i} \geqslant \sum{F_i} => \text{No está en trashing}$ 
			 Cant de frames en memoria
Asignación Fija:
	$CT_i \leqslant CF_i => No está en trashing$ 
	CF = Cant de frames asignados al proceso