![[Pasted image 20241028151225.png]]
Static Content:
	Ningún microservicio debería tener el contenido estático
	Se saca hacia otro servicio 
___
![[Pasted image 20241028144029.png]]

# Características
- Servicios son pequeños e independientes (**débilmente acoplados**)
- Cada servicio tiene **código base independiente**, que puede administrarse por equipos pequeños independientes
- Cada equipo conserva sus propios datos o estado externo
- Servicios se comunican por **API**
- Servicios no necesitan compartir misma stack tecnológico