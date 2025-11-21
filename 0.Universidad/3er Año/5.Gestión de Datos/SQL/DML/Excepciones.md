```sql
BEGIN TRY
	...
END TRY
BEGIN CATCH
	...
END CATCH
```
___
# RaiseError
**No** corta el flujo ejecución
```sql
BEGIN CATCH
	raiserror('Error en el catch', 16, 1);
END CATCH
```
# Throw
**Si** corta el flujo de ejecución
```sql
BEGIN CATCH
	throw 50000, 'Error en el catch', 1
END CATCH
```