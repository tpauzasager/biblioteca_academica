ESQUEMA INDEXADO

# INODO
Son los FCB pero con más cosas 

![[Pasted image 20241101225008.png]]

Single indirect: 
	Puntero simple del esquema indexado (a bloque de punteros) 
Double indirect:
	Apuntan a un bloque de punteros de otros bloques de punteros 
___
## Estructura
| Sector de Partida | Grupo de bloques 0 | Grupo de bloques 1 | ... |
| ----------------- | ------------------ | ------------------ | --- |
Por cada Grupo de bloques 

| Super Bloque                                          | Descripctores de grupo                                                                     | Bitmap datos | Bitmap inodos | Tabla de Inodos | Blqoue datos |
| ----------------------------------------------------- | ------------------------------------------------------------------------------------------ | ------------ | ------------- | --------------- | ------------ |
| - Total Nodo/Bloques/Libres<br>- Tamañoo bloque/Inodo | - Bloque de bitmap de datos/inodos<br>- Bloques libres en grupo<br>- Inodos libres en gupo |              |               |                 |              |
___
# Directorio