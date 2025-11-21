# Segmentación 
Divide memoria en segmentos de longitud variable

# Paginación 
Divide memoria en páginas de misma longitud fija (usado por MBD)

![[Pasted image 20241008170813.png]]
Componentes:
	- Id: Identificador de pág
	- Body: Información almacenada (renglon es mín unidad de asignación)
	- Footer offset: Indice de la pág (cada uno refiere a un renglon de la pág) 

Fragmentación:
	- Externa: página de menor tamaño al del cluster (por el cual asgian espacio el disco) => Se extiende página para que tenga tamaño parecido al cluster
	- Interna: Fila a almacenar es más pequeña (o más grande) que el renglón de la pág
___
# Clustering
Agrupamiento de objetos según criterio 

Métodos: 

| Método     | Descripción                                                                                                                                     |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Intra-File | Objetos agrupados en función de pertenencia a conjunto predeterminado<br>Ej: Todos los clientes                                                 |
| Inter-File | Objetos agrupados en función de relación entre objetos (no depende de si pertenecen a diferentes conjuntos)<br>Ej: Cliente y todas sus facturas |
## En DBMS

| Método     | Descripción                                                                     |
| ---------- | ------------------------------------------------------------------------------- |
| Intra-File | En página solo pone filas de una misma tabla (no mezcla tablas en misma página) |
| Inter-File | Almacena indices y PK asociadas a FK                                            |
___
# Almacenamiento Interno
Header de tablas:
	DBMS crea header para identificar tablas (columnas, longitud, cant filas, etc.)
