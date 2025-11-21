| Tipo        | Descripción                                     |
| ----------- | ----------------------------------------------- |
| Con Pérdida | No son reversibles<br>Para archivos multimedia  |
| Sin Pérdida | Son reversibles <br>Para archivos no multimedia |
Capacidad desperdiciada:
	- Alfabeto ASCII tiene longitud fija y, por más que se repita el mismo caŕacter, este ocupara el mismo espacio tantas veces como se repita
	- No todos los archicos utilizan todos los caracteres ASCII, por lo que se desperdician bits 

___
# Algoritmo de Huffman
Caracteristicas:
	- No tiene perdida 
	- Eficiente para archivos de texto
Concepto:
	- Define código variable para cada carácter del archivo (sin usar prefijos)

## Tabla de frecuencias
Relaciona cada carácter con su frecuencia de aparición y un código que lo identifica 

## Árbol binario 
Componentes:
	Raíz:
		- Contiene la sumatoria de las frecuencias de todos los caracteres del archivo 
	Nodo: 
		- Padre
		- Sumatoria de frecuencias de los demás nodos
		- Hijo izq (0) / der(1)
	Hoja: 
		- Frecuencia
		- Código identificador
Decodificación: 
	Con el tren de bits leídos, se recorre el árbol (0 -> hijo izq; 1 -> hijo der) y se obtiene el carácter 
Codificación:
	Se le asigna una posición del árbol a cada carácter y se lee desde esa posición hasta llegar a la raíz, para así obtener el código correspondiente a esa posición (priorizando que los carácteres con mayor frecuencia tengan un código más corto)

## Pila
Se usa para que, a medida que se va recorriendo el arbol, se guarda 0(izq) o 1(der) hasta llegar al caracter especifico 