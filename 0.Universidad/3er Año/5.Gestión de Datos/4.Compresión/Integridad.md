# Integridad
Valida que un archivo no haya sufrido cambios (sea por tranferencia, compresión y descompresión, etc)

Control:
	- Cuando se comprime y descomprime un archivo, se necesita verificar que el nuevo archivo sea igual al original 
Procedimiento: 
	- Existen métodos para controlar sin contar con el archivo original 
	- Comparación: 
		- Tamaño / Contenido / Posición (de cada caracter)

## CheckSum
Utiliza un polinomio para evaluar tamaño, contenido y posición de los caracteres del archivo
	- Tamaño: Dado por el grado del polinomio
	- Contenido: Dado por coeficientes del polinomio
	- Posicón: Dada por grado que acompaña a la x del polinomio 

Funcionamiento: 
	Antes de comrpimir, se calcula el polinomio del archivo (definiendo un valor de x)
	Se agrega el resultado del polinomio en el archivo compreso
	Al descomprimir se vuelve a calcular y evaluar el polinomio del archivo resultante
	Se comparan resultados 

Ej:
	"HOLA"  $=> ~p(x) = Hx^0 + Ox¹ + Lx² + Ax³$
	Realidad: Se usan los bits que forman los caractreres (cambiar letras por 0 o 1 en función del caracter que se quiere representar)

# CRC 
(Control de Redundancia Cíclica)
Utiliza **CheckSum** para la validación de integridad
Es redundante porque se trata de una suma que esta de más y no afecta a la compresión o descompresión del archivo

