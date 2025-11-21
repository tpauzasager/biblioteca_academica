# Fetch
Funcionamiento: 
	Buscar la próxima instrucción a ajecutar
___
# Decode
Funcionamiento:
	Interpretar que instrucción es la que se va a ejecutar (requiere traducción de dir lógica a dir física)
___
# Execute
Funcionamiento:
	Ejecución de la instrucción correspondiente 
	Al finalizar la ejecución, el PC es incrementado en 1 (a no ser que sea modificado por una instrucción)
___
# Chech Interrupt
Funcionamiento: 
	Se verifica si KERNEL envió alguna interrupción al TID en ejecución
	Si hay interrupción => Se actualiza contexto de la MEMORIA y se devuelve el TID al kernel junto al motivo de la interrupción
