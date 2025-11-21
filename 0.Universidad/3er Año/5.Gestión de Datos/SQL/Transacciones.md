
| Nombres           | Dirty Read | Repeatable Read | Phantom Read |
| ----------------- | ---------- | --------------- | ------------ |
| Read Uncommitted  | Si         | No              | Si           |
| Read Committed    | No         | No              | Si           |
| Repeatable Read   | No         | Si              | Si           |
| Serializable Read | No         | Si              | No           |
Dirty Read:
	Se pueden leer datos no commiteados
Repeatable Read:
	Es misma transacción se asegura que la consulta da siempre el mismo resultado (pero pueden aparacer nuevas filas que no hayan estado antes)
Phantom Read:
	Aparecen filas nuevas insertadas desde otra transacción 
___
Tiene propiedaes **ACID**
___
# DeadLock
Se genera cuando dos o más transacciónes pretenede operar sobre tablas bloqueadas por las demás, por ende, ningúna puede seguir avanzando 
Manejo:
	Se finaliza la última transacción inciada
___
```sql
BEGIN TRANSACTION
	...
[COMMIT, ROLLBACK] TRANSACTION
```
