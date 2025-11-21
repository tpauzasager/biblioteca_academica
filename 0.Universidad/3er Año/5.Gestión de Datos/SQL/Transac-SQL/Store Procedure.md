```sql
CREATE PROCEDURE nom_procedure (@param_entrada dataType, @param_salida dataType OUT, ...) AS
BEGIN
	...
	RETURN @var
END
```
___
Puede devolver varios resultados
Puede ser invocada en Consulta u operación DML
Puede ejecutar culquier instrucción DML 