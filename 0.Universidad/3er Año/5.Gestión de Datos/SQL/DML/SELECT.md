```sql
select 
	from 
	[left, right, full] join
	where ... [and, or] ...
	group by 
	having 
	order by 
```
___
# Case 
```sql
select   
	case
		when nombre_col = "val_esperado" then "val_resultado"  
		when nombre_col < "otro_val" and ... then "otro_res"
		else "default"
	end nombre_columna_en_select
```
# Join
```sql
select val1 
	from tabla t1
		join tabla2 t2 on t2.val = t1.val // Solo muestra filas con coincidiencia en ambas tablas
		left join ... // Además muestra valores de tabla dominante (izq) que no hayan tenido coincidencia con la otra tabla a joinear 
		right join ... // Mismo, al revés
		full join ... // Muestra todas las filas, haya o no coincidencia 
```
# Group by
```sql
select sum(val1)
	from tabla
	group by val2,val3
	
// Toda columna del select no afectada por func de agregación tiene que estar en group by
```
# Having
```sql
select sum(val1)
	from ...
	group by ...
	having sum(val1) > 40  //Solo muestra columnas que cumplan
```
___
# COALESCE
```sql
Select COALESCE(nom_col, 'val_default') AS nom_col_resultado
	FROM ... 
```