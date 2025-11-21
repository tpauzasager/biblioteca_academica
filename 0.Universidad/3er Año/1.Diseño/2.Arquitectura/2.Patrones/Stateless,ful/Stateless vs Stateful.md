# Componentes de Modelo

| Stateless                                                                                                         | Stateful                                                                     |
| ----------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| - Componente aislado<br>- No se guarda info sobre operaciones anteriores<br>- Cada op es como si fuera la primera | - Componente que recuerdan su estado<br>- Op afectadas por las op anteriores |
![[Pasted image 20241028113012.png]]
___
# Web
| Stateless                                                                                                                          | Stateful                                                                                                                                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| - No se almacena sesión en el servidor<br>- Usuario tiene que identificarse en cada solicitud (con Token que el server decodifica) | - Se almacena sesión en servidor<br>- Usuario se identifica una vez<br>- En 1ra vez que se identifica (inicia sesión) server le da espacio en memoria y un ID (seteado en la cookie)<br>- Para solicitudes posteriores, server revisa la cookie |
![[Pasted image 20241028113307.png]]