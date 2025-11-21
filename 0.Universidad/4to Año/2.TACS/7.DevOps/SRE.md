Service Management
- Todo lo que no es desarrollo de features 
- Mantenimiento 

Sysadmin approach 
- Costos -> A medida que crece el sistema, crece el costo para mantenimiento (monetario, skill set, terminologías)
- Diferencia de objetivos
	Dev -> Quiero sacar más features
	Ops -> No quiero implementar features pq se me cae el servidor 
___
Site Reliability Engeneering 
# Definición 
Implementación de DevOps (de Google)

Reliability
- Feature más importante 
- 100% disponibilidad es confiabilidad equivocada (cada servicio necesita disponibilidad diferente)
Error Budget
- Tiempo que el servicio puede estár caido 
- Para determinar tiempo entre realice (mientras más budget, puede deployear con más frecuencia)
- Para determinar si pueda entregar una nueva feature (pq si ya me consumí el error budget => no puedo arriesgar a que el servidor se caiga de nuevo )

## Metricas
SLI -> Service Level Indicator
- Medición para _successful enough_
- Tiene limite superior
- Ej -> Latencia de una request
SLO -> Service Level Objetive
- Objetivo de interacciones exitosas con el usuario
- Tiene limite superior e inferior
- Si no lo tengo bien definido => Puede sobre diseñar la solución
	Caracteristicas
		- Estandarizar indicadores 
		- Tener pocos
		- Evitar absolutos 
		- Percentiles 
SLA -> Service Level 
- Consecuencias
- SLA = SLO + margen
- Es lo que le tengo que garantizar al cliente (mantengo un margen frente al objetivo)
	Caracteristicas
		- Contrato explicito o implicito 
		- Incluye consecuencias si no se cumple 
___
# Implementación 
1. Definir los dominios discretos de dominio y seleccionar un flujo que se quiere atender
	Los dominios son de extremo a extremo (pasa por todo front y back)
2. Definir Error Budget 
	Definir SLI, SLIO, SLA y error budget
3. Alerting y Monitoreo 
	Más loggs y observabilidad 
4. Blameless 
	Culpar sistemas, no personas
	Blameess posmortem 
5. No hacer todo a la vez 
___
# Principios
- Embracing risk
- SLO
- Eliminar toil (tareas manuales que no agregan valor)
- Sistemas distribuidos de monitoreo
- Automatización (para deploy/entrega)
- Realise engineering 
- Simplicidad 