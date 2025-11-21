Estructura de datos unívoca (tiene un solo predecesor, pero muchos sucesores)

# Pripiedades
| Nombre   | Definición                                     |
| -------- | ---------------------------------------------- |
| Dirigido | Relaciones tiene dirección                     |
| Acíclico | No hay ciclos                                  |
|          | Existe camino único entre cada par de nodos    |
|          | $\text{cant vertices}= \text{cant aristas}+ 1$ |

# Caracteristicas
| Nombre      | Definición                                                          |
| ----------- | ------------------------------------------------------------------- |
| Grado       | Cant máx de hijos                                                   |
| Nivel       | Altura de cada nodo (raíz en nivel 0)                               |
| Profundidad | Nivel máx                                                           |
| Crecimiento | $\color{yellow}\text{cant máx elementos} = {grado}^{profundidad}-1$ |
# Clasificación  
- Las busquedas se realizan por nivel, no por elemento. Esto hace que sea más eficiente buscar dentro de un árbol 

| Nombre                   | Definición                                                                           |
| ------------------------ | ------------------------------------------------------------------------------------ |
| Completo                 | Todo nodo cumple con grado del árbol o es hoja<br>Lleno => Todas hojas a mismo nivel |
| Balanceado               | Caulquier camino desde la raíz a una hoja tiene misma longitud (o difiere en 1)      |
| Perfectamente Balanceado | Balanceado en cada nivel<br>Tiene más cant de lementos en cada nivel                 |
