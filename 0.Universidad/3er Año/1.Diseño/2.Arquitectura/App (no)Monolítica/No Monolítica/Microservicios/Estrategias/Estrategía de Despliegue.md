# Blue/Green Deployment
 ![[Pasted image 20241028172227.png]]
Development:
	
QA:
	Testers realizan primeras pruebas sobre lo desarrollado
Staging:
	Ambiente de test, donde se suman más actores a probar todas las soluciones
Producción:
	- LLeva de a pocos usuarios a la nueva solución 
	- Esto es rápido para que no haya incosistencias con los usuarios
___
# Canary
![[Pasted image 20241028172243.png]]

Funcionamiento:
	- A medida que usuarios realizan operaciones, se los va moviendo hacia la nueva solución 
	- Estrategía más paulativa 
	- Si se detectan errores, se devuelven los usuarios al servicio antiguo 