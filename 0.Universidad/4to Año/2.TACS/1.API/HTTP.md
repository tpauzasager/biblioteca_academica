# HTTP Request 
- Dominio -> `ejemplo.com`
- Recurso -> `/usuarios` o `/favicon.png`
- Query params -> `?id=1234`
- Método -> GET, POST, PUT, UPDATE, DELETE
- Header -> Info extra del servidor 
- Body
## Verbos
Seguridad -> Ejecución no tiene efectos secundarios
Idempotencia -> Estado del recurso se mantiene en ejecuciones subsecuentes del verbo (independientemente de cuantas veces seguidas se ejecute)

| Verbo   | Seguridad | Idempotencia | Función                           |
| ------- | --------- | ------------ | --------------------------------- |
| GET     | x         | x            | Traer recurso                     |
| OPTIONS | x         | x            | Operaciones sobre un recurso      |
| PUT     |           | x            | Modifcar recurso                  |
| DELETE  |           | x            | Eliminar recurso                  |
| PATCH   |           | (x)          | Modificar parcialmente un recurso |
| POST    |           |              | Crear recurso                     |
patch puede no ser idempotente (que pasa si hago a++ en el recurso?)
Si es Seguro e Idempotente => **Es cacheable**
En necesario que flujos importantes del modelo sean idempotentes

# Status Code

| Cod | Uso                            | Ejemplos                                                                          |
| --- | ------------------------------ | --------------------------------------------------------------------------------- |
| 1xx | Respuesta intermedia           | Para informar al cliente antes de mandar respuesta final                          |
| 2xx | Success                        | 200 - OK<br>201 - Created<br>204 - No contet (response sin body)                  |
| 3xx | Variado<br>(redirects y cache) | 301 - Movido permanentemente<br>304 - No modificado<br>307 - Movido temporalmente |
| 4xx | Cliente error                  | 400 - Bad request<br>401 - No autorizado<br>403 - Forbidden<br>404 - Not found    |
| 5xx | Server error                   | 500 - Internal server error<br>503 - Service unavailable<br>504 - Gateway timeout |
