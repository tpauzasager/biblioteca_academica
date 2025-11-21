![[Pasted image 20241101221514.png]]

Esquema BLOQUES ENLAZADOS 

# Tabla FAT
- Se guarda en memoria
- Contiene punteros al siguiente bloque del archivo 
- Se guarda al inicio del FS (se copia a memoria)
___
# Caracteristicas
- Permite acceso directo 
- A disco se accede una vez por bloque (cluster)
- Entrada indica bloque que le sigue 
- **No tiene FCB** (info administrativa se guarda en entradas a directorios)
- Bloques libres administrados recorriendo la tabla 
____
## Estructura

| Sector de Arranque | FAT + copia | Directorio Raís | Datos |
| ------------------ | ----------- | --------------- | ----- |
Directorio Raíz: 
	- Cant fija de entradas de tamaño fijo
	- Atributos de archivo guardados en su directorio
____
# Tipos
FAT N:
	- Punteros de la tabla tienen N bits
	- Puede direccionar hasta 2^n bits
	- Tamaño máx de archivo limitado por la entrada al directorio ($2^{tamEntrada}*tamCluster$ GB)
	- Tamaño FAT = $cantEntradas * tamEntradas$ 

