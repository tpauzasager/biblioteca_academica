Resultado de ejecución depende del orden particular determinado por planificador 
Dificil de detectar porque no es un error como tal y aveces puede dar resultados coherentes
## Condiciones de Bernstein   
- Varios procesos/hilos manipulan un mismo recurso
- Al menos uno los está modificando 
- Los accesos al recurso de realizan de forma concurrente
# Sección Crítica
![[Pasted image 20240906211233.png]]
- Debe ser lo más pequeña posible 
- Debe estar rodeada por protocolo de entrada y salida 
___
# Requisitos de la Solución
1. Mutua Exclusión
	- Solo un proceso puede acceder a la sección crítica a la vez 
2. Progreso
	- La decisión de quien puede o no ejecutar la sección crítica se toma en función de aquellos procesos que la están ejecutando y aquellos que están en la sección de entrada
3. Espera Limitada
	- No debe haber starvation. Hay un tiempo límite en la cantidad de veces que otro proceso ingresa antes que el 
4. Velocidad de los Hilo 
	- Solución debe funcionar independientemente de como los procesos uses la sección crítica 

## Solución a nivel SW 
ver resumen Programming
## Solución a nivel HW

| Nombre                                | Descripción                                                                                                                                                                                                          | Caracteristicas           |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| Deshabilitar interrupciones           | - Se realiza a nivel kernel<br>- No lo puede hacer el usuario<br>- Si hay varias CPU, aumenta mucho el costo (ya que se deshabilitan en todos)                                                                       | - No genera espera activa |
| Instrucciones Atómicas (test and set) | - Instrucción atómica para verificar y modificar un valor en memoria de manera indivisible<br>- Lee valor en memoria (boolean). Si es 0, devuleve 0 y luego lo cambia a 1. Si ya es 1, devuelve 1 (y no cambia nada) | - Genera espera activa    |
## Solución de Peterson
- Solo funciona para 2 procesos
- Proporciona
	- Muta exclusión 
	- Progreso
	- Espera limitada 

## Solución de SO
SEMÁFOROS