Definición:
	- Evitar que dos procesos escriban sobre mismo archivo al mismo tiempo 
	- Mantiene integridad de archivos 

Tipos:
	Exclusivo:
		- Solo un proceso puede tenerlo. 
		- No permite que el resto acceda
	Compartido:
		- Muchos procesos pueden tenerlo
		- Un proceso no puede tener uno exclusivo si haya uno compartido
	Obligatorio:
		- SO asegura que ningún otro proceso podrá usar el archivo
		- Costo: Más tiempo de espera para los procesos
	Sugerido:
		- SO da info del estado del lock, pero responsabilidad queda por el programador 