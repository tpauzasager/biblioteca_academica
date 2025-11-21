Funciones:
	- Estructura opcional asociada a tabla, pero logica y fisicamente independiente (se puede crear y borrar en cualquier momento)
	- Permite rapido acceso a datos de la tabla
___
# Caracteristicas
- Unicidad:
	- Unique -> No permite claves duplicadas
	- Duplicado -> Si permite 
- Simple -> Clave compuesta por unica columna
- Compuesto -> Clave compuesta por varias columnas
___
# Tipos
## Btree
- No es lo mismo que un árbol binario (pero parece ser lo mismo)
- Tiene las PK ordenadas y puntero a la posición de la tabla
## Btree Cluster
- Las hojas poseen todos los datos de la fila
## Bitmap
- Util para pocas claves con mucha repetición 
## Hash
- Implementada a partir de tablas hash
## Functional
- Para tablas cuya PK deriva de resultado de una función 
## Reverse Key
- Invierte los bytes de la PK indexada
- Para cuando PK es serie con crecimiento constante (ej: numeral con crecimiento de uno a uno)
## Btree +
- Indice Btree, pero los nodos (intermedios) están linkeados, facilitando lectura secuancial
- No está ordenado
___
# Ventajas vs Costos
| Ventaja                                                                            | Costo                                                                                                |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| - Eficiencia en ordenamiento<br>- Asegura cumplimiento de constraints (PK, FK,etc) | - Ocupa espacio en disco<br>- Cada vez que se modifica la tabla, el indice tendrá que ser modificado |