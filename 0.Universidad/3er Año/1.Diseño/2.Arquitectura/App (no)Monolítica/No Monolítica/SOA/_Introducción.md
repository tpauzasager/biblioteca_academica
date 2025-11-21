Service Oriented Architecture

# Definición
- Orientado a Estrcutura Organizacional (**enterprise**)
- Descompone lógica funcional de aplicación en unidades autónomas 
- Cada servicio consume a los demás, pero núnca sabe quien es exactamente lo que consume (solo se sabe el contrato)
- Cada servicio puede implementar la arquitectura independientemente 

# Principios
- Se reutilizan servicios
- Metas estratégicas por encima de beneficios específicos de proyectos
- No hay integración directa entre sistemas. Solo se conocen los contratos (interoperabilidad)
- Si hay servicio que resulve problema, no se vuelve a desarrollar
- Flexibilidad por encima de optimización 
- Refinamiento Evolutivo encima de búsqueda de perfección inical

# Actores
![[Pasted image 20241028124700.png]]

| Nombre     | Descripción                                                                                                                                                                                                    |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Consumidor | Servicio que demanda funcioanlidad proporcionada por otro servicio                                                                                                                                             |
| Proveedor  | Entidad accesible a través de la red que acepta y ejecuta consultas de consumidores<br>Publica sus servicios y contrato de interfaces en registro de servicios (para que consumidor pueda acceder al servicio) |
| Registro   | Repositorio de servicios disponilbes<br>Permite visualizar interfaces de poveedores a los consumidores interesados                                                                                             |
___