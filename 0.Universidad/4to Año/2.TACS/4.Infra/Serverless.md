# Definición 
- FaaS (Function as a Service)
- Código propio que corre en una plataforma de 3ros sobre containers efimeros (como SaaS)
- **Orientado a eventos**
- Optimiza costo y complejidad de escala 
- Hay **vendor locking** fuerte
- Lifecycle de mi función 
	1. Cold start
	2. Ejecutar
	3. Stand by (corto por si tengo otra request en el corto plazo)
	4. Muerte
- Donde usarlos:
	- Problemas simples y puntuales 

Pros:
	- Simplicidad en operación IT
	- Alta escalabilidad 
	- Bajo costo 
	- Confiabilidad
	- Pagas por el tiempo de ejecución 
	- Microservicios
	- Inmutable (no se puede modificar la instancia)
	- Polyglota (muchos lenguajes)
Cons:
	- Governance (equipo tiene que ser capacitado y estár de acuerdo)
	- Observabilidad
	- Debugging
	- Orquestación compleja