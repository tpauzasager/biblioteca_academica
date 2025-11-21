# Valores del Header 
___
cache-control: {no--cache, no--store, private, public, max-age=3600}
___
ETag: "id" -> Hash de la response
If-None-Match: id

1. Cliente hace request 
2. Server responde con response y el etag
3. Proxima request del cliente agrega el If-None-Match: [ETag]
4. Si contenido cambio => 200 y vuelve a envíar el contenido
	Si contenido no cambió => 304 (not modified) y no vuelve a envíar el contenido

Caso de uso:
	- Para controlar que alguien modifique un recurso que no conozco de ante mano, fuerzo que verbos como PUT viajen con el "If-match"
	- ej: (se puede hacer con PATCH o UPDATE)
		1. GET /users/1234  ;  ETag: "555"
		2. PUT /users/1234 ; If-match: "555"
	- Así prevengo condición de carrera sobre el recurso porque, si se modifico el recurso, te va a rebotar la request PUT
___
Vary: Accept-Encoding (ejemplo)

Indica que ignorar para determinar si el contenido está o no cacheado 

# Diagrama
![[Pasted image 20250903193104.webp]]
## Ejemplo Etag
![[Pasted image 20250903193519.webp]]