# Temporal
Local -> #nombre_tabla
Global -> ##nombre_tabla
```sql
// Explicita
CREATE TABLE #nombre_tabla(
	nom_colum tipoDato,
	...
);

// Implicita
SELECT * INTO #nombre_tabla
	from nom_tab
	...
```
# Constraints
```sql
CREATE TABLE nombre_tabla(
	nom_col tipoDato PRIMARY KEY,
	... REFERENCES nom_tab,
	... DEFAULT 5,
	... NOT NULL,
	... UNIQUE, 
	nom_col2 tipoDato CHECK(nom_col2 > 42),

	PRIMARY KEY (nom_col, nom_col2, ...)
	FOREIGN KEY (nom_col, nom_col2, ...) REFERENCES nom_tabla2
	UNIQUE (nom_col, ...)
	CHEACK (condición) //Pueden compararse entre más de una columna
);
```

