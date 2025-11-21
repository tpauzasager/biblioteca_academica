Objetivo:
	- Tratar al archivo como acceso a memoria 

Solución:
	- Asocial lógicamente con el archivo una parte del espacio virutal de direcciones del proceso 
	- Luego de cargarse, los IO al archivo se gestionan como acceso a memoria (porque eso son)

![[Pasted image 20241101202104.png]]

Ventajas:
	- Disminuye overhead (de syscalls de read y write) 
	- Favorece compartición de archivos entre procesos
	- Escrituras no se realizan sincrónicamente (no necesariamente)