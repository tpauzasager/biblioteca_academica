# Definición 
Conjunto de normas y restricciones para el diseño de APIs sobre HTTP
## Caracteristicas

| Caract                         | Definición                                                                                                                                                                                       |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Arquitectura                   | Cliente <-> Servidor                                                                                                                                                                             |
| Stateless                      | Servidor no guarda estado previo del cliente<br>Cada request lleva info necesaria para poder contestar sin contexto previo<br>Independencia entre requests<br>Ayuda **escalabilidad horizontal** |
| Cache aware                    | Respuestas tiene que poder ser cacheables                                                                                                                                                        |
| Interfaz uniforme              | Recursos definidos con sustantivos plurales y id son unicos                                                                                                                                      |
| Sistema de capas               | Pueden haber muchas capas, pero el cliente no le importa porque capas pasa su request                                                                                                            |
| Código bajo demanda (opcional) | Servidor da a cliente código para que lo ejecute                                                                                                                                                 |
# Nivel de Maduración 

| Nivel | Def                        | Caracteristica                                |
| ----- | -------------------------- | --------------------------------------------- |
| 0     | Swap of POX                | -                                             |
| 1     | Resources                  | Sustantivos (en plural) para definir recursos |
| 2     | HTTP Verbs<br>Status Codes | Buen uso de verbos                            |
| 3     | HATEOAS                    | Navegabilidad <br>Discovery                   |
___
Versionado
- Es importante para no romper con contrato con el cliente (si genero cambios que rompen con interfaz => tengo que seguir permitiendo que cliente me acceda de la misma forma hasta ahora)