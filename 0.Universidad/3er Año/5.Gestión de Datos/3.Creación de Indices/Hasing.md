# Definición 
Una función hash $h(x): N -> N$ , para calcular el valor hash de la clave
Para búsqueda, inserción y eliminación, tiene orden de complejidad O(1)

| Desventajas                                                                                                                             | Ventajas                                                                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| - Perdida de información (valor hash no da info acerca de la clave)<br>- No se puede buscar mínimo, máximo u ordenar por valor de clave | - Inserción, búsqueda y eliminación en tabla hash O(1)<br>- Flexibilidad para balancear uso de memoria o tiempo [[0.Universidad/3er Año/5.Gestión de Datos/Aclaraciones\|Aclaración 1]]<br> |
# Características
| Nombre                | Descripción                                   |
| --------------------- | --------------------------------------------- |
| Evitar colisiones     | Reducir al mínimo la probabilidad de colisión |
| Distribución uniforme |                                               |
| Fácil de calcular     |                                               |
- Tabla hash siempre es menor al dominio de entrada
# Métodos
| Nombre         | Descripción                                                                                                                                                                                                                 |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| División       | Utiliza el resto de la división entre el valor de entrada y un valor M<br>M suele ser primo (para evitar sesgos)                                                                                                            |
| Multiplicación | 1. Definir tamaño $2^m$ del espacio del valor hash<br>2. Elegir constante 0 < A < 1  ;  irracional<br>3. Multiplicar clave por A<br>4. Multiplicar parte fraccionario del resultado por $2^m$<br>5. Resultado es valor hash |
___
# Resolución de Colisiones
## Encadenamiento
![[Pasted image 20240922155556.png]]
Ventajas: 
- Puede nunca requerir de crecimiento (degradación lineal)
Desventajas:
- Pobre rendimiento de caché
## Abierto
| Nombre            | Descripción                          | Primary clustering | Límite capacidad | Restricción de tamaño |
| ----------------- | ------------------------------------ | ------------------ | ---------------- | --------------------- |
| Sondeo Lineal     | ![[Pasted image 20240922162819.png]] | Si                 | -                | -                     |
| Sondeo Cuadrático | ![[Pasted image 20240922162742.png]] | No                 | $\lambda < 1/2$  | M primo               |
| Hashing Doble     | ![[Pasted image 20240922162722.png]] | No                 | -                | M primo               |
### Hashing Doble
Se tiene una 2da función hash para determinar el valor del sondeo 
Tamaño de tabla debe ser primo (porque si no se generan bucles de sondeo)