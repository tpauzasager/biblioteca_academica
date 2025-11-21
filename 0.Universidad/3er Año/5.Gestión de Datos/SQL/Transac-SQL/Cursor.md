```sql
DECLARE @var1 int, @var2 int, ... ;

DECLARE nom_cursor CURSOR 
	FOR SELECT ... ;

OPEN nom_cursor;

//Guardar val de filas obtenidas en resultado de query del cursor
FETECH NEXT FROM nom_cursor INTO @var1, @var2, ...;

WHILE @@FETCH_SATATUS = 0
BEGIN
	...
	FETECH NEXT FROM nom_cursor INTO @var1, @var2, ...;
END

CLOSE nom_cursor;
DEALLOCATE nom_cursor; 
```