# Soft-Link
Definición:
	- Requiere un nuevo Inodo
	- Archivo aparte que tiene path a otro archivo (en su propio inodo)
	- Independiente del archivo linkeado 
	- Se puede hacer hacia un directorio 
___
# Hard-Link
Definición:
	- No requiere crear un nuevo Inodo
	- Apunta al mismo inodo (el inodo tiene contador de referencias)
	- Si se borra una entrada de dir y indodo tiene HL => No se elimina el archivo, se espera a que se eliminen todos los HL
	- Se trata como un arhivo regular 
	- No se puede hacer hacia un directorio 

En FAT:
	- Se copia toda la metadata del directorio 


| Caract                    | Soft                                                                        | Hard                 |
| ------------------------- | --------------------------------------------------------------------------- | -------------------- |
| Descripción               | Archivo que tiene puntero (del inodo) que apunta hacia path de otro archivo | Apunta a mismo inodo |
| Entre volumenes           | Si                                                                          | No                   |
| Hacia directorios         | Si                                                                          | No                   |
| Independiente del archivo | No                                                                          | Si                   |
