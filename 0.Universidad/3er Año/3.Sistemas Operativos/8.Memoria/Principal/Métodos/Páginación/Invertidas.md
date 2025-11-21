Objetivo:
	- Utilizar la menor cantidad de memoria posible 
	- Se tiene una sola tabla para todo el sistema
	- Cada elemento (compuesto por pid y nro pág) representa el nro de marco 

Acceso:
	- A partir del pid y el nro de pág, se busca el elemento coincidente. La posición del elemento en la tabla es el nro de marco 
	- Para realizar la búsqueda se basa en una función hash

| Ventajas                     | Desventajas                                                                                                                                  |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| - Ocupa menos espacio en mem | - Requiere búsqueda lineal (se puede mejorar con función hash)<br>- Dificil para compartir memoria<br>- Difícil para implementar Mem Virtual |