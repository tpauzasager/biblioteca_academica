# Sincronico
Definición:
	- Cuando componente A usa una funcionalidad expuesta por B y se **queda esperando la respuesta** 
	- Forma más simple 
	- Fromato de envío de mensajes entre objetos default
___
# Asincronico
Definición:
	- Cuando A usa a B y **no se queda esperando**
	- Para no penalizar toda la ejecución del sistema 

Motivos de uso:
	- Puede continuar ejecución sin necesidad de la respuesta 
	- No importa la respuesta
	- No le pedia nada, solo avisaba

## Tipo de Respuesta
- Como hacer para que A se entere cuando B termino de procesar su llamado? 

| Nombre     | Puede generar espera activa? | Descripción                                                                                                      |
| ---------- | ---------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Pull-Based | SI                           | Periodicamente lee un espacio en memoria compartido con B (donde B deposita el resultado)                        |
| Push-Based | NO                           | Se le envía a B un **callback** que ejecuta cuando termino de ejecutar <br>Si ambos son en Web => Es **webhook** |
