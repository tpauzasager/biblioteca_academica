# M-Ario
Arbos de grando m (cuanto más grande menor tiempo de acceso y menor cantidad de accesos a memoria)

# Árbol B
![[Pasted image 20241016190853.png]]

Minimiza IO hacia el disco

Nodos:
	Hoja: Valores de las claves y punteros con posición relativa de datos secuenciales
	Raíz/Rama: Valor de la clave y puntero hacia nodo con claves menores que ella

Operaciones:

| Operación   | Descripción                                                                                                                                                                                                               |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Búsqueda    |                                                                                                                                                                                                                           |
| Inserción   |                                                                                                                                                                                                                           |
| Split       | Cuando hoja no tiene más espacio para insertar nodos.<br>La hoja para a ser una rama y sus hijos son dos nodos conformados por una mitad (cada uno) de la hoja original                                                   |
| Eliminación |                                                                                                                                                                                                                           |
| Fusión      | uando nodo cae por debajo de cant minima de elementos (usualmente mitad del máximo) se intenta:<br>Fusionar con hoja hermana (en caso de está tambien este por debajo del límite)<br>Pedir un elemento a una hoja hermana |
