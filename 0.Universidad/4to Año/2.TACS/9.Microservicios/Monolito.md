# Definición 
Aplicación donde son _toda la solución_

Ventajas
	- Simple
	- Baja latencia 
	- Unico artefacto deployeable 
	- Observabilidad más sencilla (ciclo de vida de request más facil de seguir)
	- Facil de extender funcionalidades (que usa algo que ya hay)
		- BD
		- Librerias

Desventajas
	- Deploys muy grandes 
	- No escala en cantidad de devs
	- Tiempo alto de compilación / testing
	- Codigo viejo conviviendo con código nuevo 
	- Un problema impacta en todas las funcionalidades
	- Limites poco claros entre modulos 
	- Diferentes funcionalidades requieren infraestructura / configuración diferentes (y no se pueden separar si están en monolito)
	- No se puede tener varios stack tecnologicos (lenguaje, framework, bd)

Deploys
	- Tienen que haber especialistas de cada modulo (muchos equipos resposables de cada deply)
	- Alta frecuencia de deploys (pq cada cambio de cada equipo genera un full deploy)
	- Disruptivo
___
