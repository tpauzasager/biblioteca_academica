# Comparación
| Nombre     | Caso medio    | Peor caso     | Estable | In situ | Comentario                                               |
| ---------- | ------------- | ------------- | ------- | ------- | -------------------------------------------------------- |
| Shell Sort | $O(n^{3/2})$  | $O(n^{2})$    | Si      | No      | Depende del gap<br>                                      |
| Merge Sort | $O(n·log(n))$ | $O(n·log(n))$ | Si      | No      | Util para trabajo en serie<br>Siempre misma complejidad  |
| Heap Sort  | $O(n·log(n))$ | $O(n·log(n))$ | No      | Si      | Acotado en el tiempo, usado para grande volumen de datos |
| QuickSort  | $O(n·log(n))$ | $O(n²)$       | No      | Si      | Más rápido en práctica, implementado en muchos sistemas  |
___
# Shell Sort
Funcionamiento
1. Compara elementos de la colección separados por n espacios (gap)
2. Se repite el proceso disminuyendo el valor del gap 
3. Finaliza realizando un Insertion Sort (gap = 1)
Usualmente se utiliza un gap de la mitad de la lista y se va dividiendo a la mitad
___
# Merge Sort 
Es recursivo
Conveniente cuando se tiene mucha memoria y se requiere un método que siempre tarde lo mismo 
No es in situ
Funcionamiento
1. Subdivide lista hasta obtener unas ordenadas o con 1 elemento
2. Se fusionan las sublistas hasta obtener la lista de tamaño original

Fusión lineal de dos vectores:
	1. Se toma el 1er valor de cada vector y se los posiciona ordenadamente en un nuevo vector
	2. Se toma el siguiente elemento de cada vector y se los coloca en el nuevo vector de forma ordenada
	3. Repetir hasta recorrer ambos vectores 
___
# Heap Sort
Es recursivo
No requiere espacio en memoria adicional (es in-situ)
Ejecutado en sistemas embebidos con restricciones de tiempo real 
Funcionamiento
1. Creación del árbol binario completo de búsqueda y se lo ordena
2. Se va quitando la raíz (que es el mayor valor del árbol) y se lo guarda en el vector ordenado
___
# Quick Sort 
Es recursivo
Más ampliamente usado
Facil implementación y poco consumo de recursos (es in situ)
Funcionamiento
1. Se elije un pivote y se divide a la mitad la lista (una mitad con los elementos menores al pivote y la otra con los mayores), el pivote queda fuera de las sublistas
2. Se vuelve a aplicar el método en las sublistas hasta que la sublista es de 1 o 2 elementos
3. Se unen todas las sublistas, agregando los pivotes entre medio de las sublistas que divide. 

	![[Pasted image 20240919183527.png]]

