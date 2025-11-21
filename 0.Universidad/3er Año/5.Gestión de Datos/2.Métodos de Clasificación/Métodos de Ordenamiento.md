# Clasificación
| Nombre          | Descripción                                                                                                                                                                                                                                                          |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Estable         | Salida mantiene orden relativo a la entreda. Si hay dos registros con mismo valor => Orden está determinado por cual estaba primero antes de ordenarlos                                                                                                              |
| In-situ         | Usa el mismo espacio ocupado o una constante cant extra de memoria<br>Menor tiempo de ejecución, al no requerir crear nueva estructura y poder soportar listas que no entrarían en memoria<br>Si no es In-situ, puede llegar a no funcionar dependiendo del contexto |
| Interno/Externo | Interno => el proceso ocurre en RAM<br>Externo => Archivo no cabe en memoria, se accede a elementos en disco secuencialmente (se extraen del disco, se procesan en RAM y se guardan en disco)                                                                        |
___
# Complejidad
Estudia costo de ejecución del algoritmo, considerando la cantidad de operaciones y la cantidad de elementos a procesar 

No se tienen en cuenta los recursos necesarios 

Conjunto P => Problemas con complejidad polinómica (a lo sumo)
Conjunto NP   => Problemas con complejidad superior
		    => No pueden ser resueltos computacionalmente
		    (no se pueden resolver en un tiempo razonable)

Evalua únicamente la cantidad de **comparaciones** 