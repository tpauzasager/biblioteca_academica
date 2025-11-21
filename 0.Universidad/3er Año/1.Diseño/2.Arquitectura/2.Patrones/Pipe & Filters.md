Patrón de **Flujo de Datos**
![[Pasted image 20241028173336.png]]

Definición:
	- Separa las tareas de un flujo de datos 
	- Cada filtro modifica el flujo, pero no guarda nada, pasa todo al siguiente filtro

Filtros:
	- **Stateless** e **independientes**
	- Tiene interfaz de entrada y de salida 
	- Cada uno puede ser implementado como un **microservicio**