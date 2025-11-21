# Definición 
Forma según se interconectan entre sí los nodos de la red 
# Tipos
## Bus y Arbol
- Todas las estaciones comparten mismo cable 
- Señal se propaga por todo el cable
- Todos reciben mensaje, pero solo lee el destinatario (dir de destino indicado en header de trama)
- Hay **mecanismos de acceso al medio** para gestionar Tx y Rx
## Anillo
- Bucle cerrado con repetidores (punto de conección de las estaciones)
- IEE 802.5
- Funcionamiento
	1. Datos van por trama
	2. Trama pasa por todas las estaciones 
	3. c/estación mira dir destino 
		Si es para ella => copia datos
		Si no => deja pasar (sin hacer nada)
	4. Trama circula por todo el canal hasta estación origen, donde se absorve 
## Estrella
- Todas las estaciones conectados a nodo central 
- c/estación tiene enlace para Tx y otro para Rx
Tipos de nodo central
1. Difusión (HUB) 
	- Reenvia a todas las estaciones
	- Hay colisiones
	- De capa 1
2. Conmutación (Switch)
	- Reenvia a destinatario (inteligencia)
	- Evita colisiones, + eficiencia
	- De capa 2

| Bus                                   | Árbol                                 | Anillo                                | Estrella                              |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| ![[Pasted image 20250825193808.webp]] | ![[Pasted image 20250825193749.webp]] | ![[Pasted image 20250825194228.webp]] | ![[Pasted image 20250825194241.webp]] |