# Definición
- Orientado a aplicativos (software/sistema)
- Única aplicación con conjunto de pequeños servicios 
- Cada microservicio ejecuta su propio proceso y se comunica con mecanismos ligeros (ej: API rest)
- La funcionalidad del aplicativo se da con el conjunto de todos los microservicios (por separado estos no sirven)
- Pueden ser escritos por diferentes lenguajes 
- Complicado para implementar concepto de sesiones (stateful) 
___
# Atributos
Agilidad:
	- Desarrollo independiente y en paralelo para los diferentes microservicios
	- Solo es necesario acordar en la interfaz 
Escalabilidad:
	- Se puede escalar solamente un aspecto del sistema (un solo microservicio)
Resiliencia:
	- Se puede adaptar al entorno (puede escalar a demanda)
___
# Consideraciones para Desarrollo 
Separar grandes Monolitos en muchos servicios pequeños:
	- Cada servicio ejecuta proceso propio
	- Un servicio por contenedor

Optimizar servicios para función única
	- Cada servicio es **altamente cohesivo** (principio de resposabilidad única)

Comunicación por API rest y Bus de Mensajes 
	- Para **evitar acoplamiento**
	- Hay **comunicación directa entre servicios**

Aplicar CI/CD por servicio
	- Cada servicio evoluciona diferente 

Aplicar decisiones de alta disponibilidad 
	- Cada servicio puede ser **escalado independientemente de los demás**
___
# Cuando utilizarlo
Aplicación ...:
- Grande que requiere alta velocidad de publicación 
- Compleja que necesita escalabilidad
- Requiere escalar dinámicamente y difícil predecir se requerirá 
- Requiere crecer rápidamente y sostenido en el tiempo, a nivel funcional 
- Dominio complejo (o muchos subdominios)
- Org que tenga pequeños equipos de desarrollo 


