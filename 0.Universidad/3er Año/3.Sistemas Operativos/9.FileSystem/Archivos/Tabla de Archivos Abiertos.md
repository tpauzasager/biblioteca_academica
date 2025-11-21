# Tabla Global de archivos abiertos
| Descriptor | Contador de aperturas | FCB |
| ---------- | --------------------- | --- |
| ...        | int                   | ... |
Contador de aperturas:
	Sirva para que (cuando llegue a cero), se persistan los cambios del archivo en el disco 

___
# Tabla de archivos abiertos del proceso
- Cada entrada es una referencia una entrada de la tabla global 