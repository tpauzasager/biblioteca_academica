 ![[Pasted image 20241105103047.png]]
Desafíos:
	- Disponibilidad
	- Velocidad de procesamiento
	- Confirmación de procesamiento

Objetivos:
	- Desacoplar mediante Mensajería
	- Modo de Transmisión: Cola o Topic

Definición:
	- Forma de comunicación asíncrona entre servicios 
	- Se usa generalmente en microservicios y sin servidor 
	- Puede persistir mensajes durante un tiempo (para poder reintentar el envío)

Funcionamiento:
	- Mensajes almacenados en cola hasta que se procesan y eliminan 
	- Cada mensaje se proceso solo una vez
	- ...
	- Permite **desacoplar** los sistemas (la cola es el intermediario)
	- Mejora rendimiento, fiabilidad y escalabilidad 
	- Permite **comunicación asíncrona**
	- Ofrece búfer ligero que almacena temporalmente los mensajes 
	- ...

Mensajes:
	- Pequeños
	- Para envíarlo, el producctor lo agrega a la cola 
	- Mensaje almacenado en cola hasta que se recupere (por el consumidor)
	- En consumidor recupera el mensaje almacenado en la cola 

Implementaciones:
	- Amazon Simple Queue Service 
	- Azure Service Bus
	- RabbitMQ
	- Active MQ
	- Apache Kafka   <<--- Se usa mucho