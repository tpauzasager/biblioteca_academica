Definición:
	Diseño de comunicación entre cliente y servidor
	Sincronica si o si 

Funcionamiento:
	- Crea solicutd HTTP que contenga todos los datos necesarios
	- Espera un RESPONSE
	- Todo objeto se manipula mediante URI (Uniform Resource Identificator)
	- Usa formatos de intercambio JSON/XML

Consideraciones:
	- Rutas siempre deben llevar nombres de recursos
	- No usar verbos como nombres de rutas 
	- Usar códigos de estado HTTP en el RESPONSE 