Tipos:
	- Acceso total: No se aplica ningúna estrategia 
	- Prohibido: Solo el **propietario**
	- Controlado: Indica quien puede o no operar sobre el 
		- Propietario | Grupo | Universo 
			- Protección de Unix
		- Matríz de acceso
			- usuario -> permisos
			- Tiene más granularidad
			- desperdicia mucho espacio
		- ACL (Access control list): 
			- Por cada archivo -> Lista de usuarios con permisos
			- Más  específico 
			- Ocupa menos espacio 
___
# Protección en Unix
![[Pasted image 20241101194533.png]]
Esta en el FCB
Si File Type == d (directorio):
	Read: ver contenido del directorio (ls)
	Write: Modificar contenido (crear/eliminar archivos)
	Execute: Poder posicionarse dentro del directorio (cd)

Cambiar Permisos (chmod):
	- Modificar todos los permisos:
		`chmod 755 myfile` 
		755 = 111 101 101  (bits del array de permisos)
___
Puede pasar que no es suficiente con Propietario, Grupo y Universo 
Para esto se puede combinar estrategia con ACL (si es necesario)

![[Pasted image 20241101195206.png]]

