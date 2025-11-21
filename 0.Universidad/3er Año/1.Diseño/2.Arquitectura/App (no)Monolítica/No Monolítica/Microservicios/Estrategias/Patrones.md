# Fachada
- Se crea clase con métodos para centralizar llamadas a diferentes componentes 
___
# Entidad y Agregado
- No se ven 
___
# Servicios
- buscar
___
# Adaptardor de Microservicios
- Se adapta una API heredada a una API RESTful 
___
# Strangler 
![[Pasted image 20241028171531.png]]
- Permite pasar de un patrón monolítico a uno de Microservicios
___
# Service Registry
- Identificar servicios e intercambiarlos agílmente
___
# Correlation ID y Log Aggregator
- Resuelve problemas de trazabilidad y seguimiento de errores 
___
# Circuit Breaker
- Detectar y cortar llamado a servicios que están funcionando incorrectamente 
- Los servicios tiene un HealthCheck que el breaker los usa para evaluar si esta funcionando bien 
___
