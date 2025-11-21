# Politicas
Asignación 
- Fija: Proceso siempre tiene asignado un número fijo de frames
- Dinámica: Proceso tiene número dinámico de frames asignados

Sustitución:
- Local: Vícitimas están dentro del conj de frames del proceso 
- Global: Se pueden elegir víctimas de cualquier frame

![[Pasted image 20241025232609.png]]
___
# Algoritmos
- Cada vez que ocurre un PF, hay operación de carga de pág (se lee pag faltante de disco y se carga en mem) y aveces de descarga (se escribe contenido del marco víctima en disco)