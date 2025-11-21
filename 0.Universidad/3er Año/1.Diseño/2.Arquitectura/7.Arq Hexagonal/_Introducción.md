![[Pasted image 20241105094903.png]]

Objetivo:
	- Permitir que lógica de negocio pueda ser utilizada por todos (usuario, programas, scripts)
	- Permite desarrollar y probar aisladamente 

Motivación:
-

Capas:
- Dominio
	- Entidades de dominio
- Aplicación
	- Casos de uso
- Infraestrucutra
	- Comunicación con exterior

Distribución de Archivos
	- PackageMain
		- Domino
		- Aplicación
		- Infraestructura

# Capas
## Dominio
- Que sea visto como una API con contratos especificos
- Se definen puertos(o interfaces) para que los otros módulos puedan implementarlas sin conocer origen de la conexión 
- Puerto -> Inertaz pública
  Adapter -> ...
