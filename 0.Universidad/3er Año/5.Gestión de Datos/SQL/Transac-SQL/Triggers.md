```sql
CREATE TRIGGER nom_trig
	ON nom_tabla
	{AFTER, INTEAD OF} [UPDATE, INSERT, DELETE]
	AS BEGIN
		..
	END
```
___
# Tablas especiales
```sql
SELECT * 
	FROM deleted //Devuelve todas las filas eliminiadas antes del procedure

SELECT *
	FROM inserted //Mismo pero con filas insertadas
```
