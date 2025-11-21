Restricciones:
	- No se pueden crear indices de vistas
	- No se le pueden agregar clausulas order by o union
```sql
CREATE VIEW nom_vista (nom_col_en_vista, ...)
AS SELECT 
	...
WITH CHECK OPTION //No deja agregar o modificar filas que no cumplan con la condición de la vista
```
___
Restricciones:
	- No se le pueden crear indices 
	- La view depende de la tabla a la que haga referencia 
	- Si tienen join => no admite Insert, Delete, Update
	- No se le puede agregar un Order by o Union