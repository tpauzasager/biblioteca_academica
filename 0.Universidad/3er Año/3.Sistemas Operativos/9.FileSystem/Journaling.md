- Info de estructuras están más actualizadas en memoria 
- Fallo en sistema puede generar inconsistencia 

Solución:
	- Se lleva un registro de las operaciones y los commits
	- Si al inicial sistema no está en un commit => rollbackea las operaciones hasta llegar a un commit 

![[Pasted image 20241101211055.png]]