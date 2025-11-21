- Ocurre sobre recursos ***REUSABLES*** 
	- Recurso que un proceso lo pide, usa y lo libera para que pueda ser usado por otro proceso (ej: semáforo mutex, memoria, etc.)
	- Pueden tener más de una instancia (ej: semáforo inicializado en 3 -> Hay 3 instancias del recursos que pueden usarse simultáneamente) 

# Definición 
Un conjunto de procesos están bloqueados y esperando un suceso producido por uno de los procesos bloqueados 
Los procesos nunca terminan de ejecutarse, ya que, los recursos permanecen ocupados, impidiendo que continue el resto de procesos

# Ejemplo
![[Pasted image 20240913185256.png]]

# Condiciones Necesarias
1. Mutua exclusión
2. Retención y espera
	- Al menos debe haber: Un recurso esperando y otro bloqueando un recurso
3. Sin desalojo
4. Espera circular `--vvvvvvvvvvvvvvvvvvvvvvvvvvv--`
![[Pasted image 20240913190356.png]]
