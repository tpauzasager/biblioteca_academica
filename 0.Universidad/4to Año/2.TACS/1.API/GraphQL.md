Caracteristicas
- Orientado a grafos 
- Agnostico al método de transporte 
- tipado 
- Paginación 
- No es necesario crear un enpoint por cliente, cada uno me pide lo que quiere y listo
- Fix:
	- Over/Under fetching -> Pedis exactamente lo que queres (ni más ni menos)
	- N+1 -> Cuando hago 1ra request para obtener una lista y depsues 1 request por cada elemento en la lista 
# Ej
## Query
![[Pasted image 20250903200958.webp]]
## Mutation
![[Pasted image 20250903201436.webp]]
explicaión: 
	Agrega nuevo registro y lo pido para poder mostrarlo 
___
# Caching 
- Usando cliente y Engine Apllo (antes del servidor GraphQL)
- No se puede cachear un POST (ya de por si es peligroso)
- Mucha customización 
___
![[Pasted image 20250903202017.webp]]
