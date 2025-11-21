# Definición 
- Administrar evolución del proyecto (versiones, cambios)
- Objetivo -> Garantizar integridad
- Auditar 

# Conceptos
## Item de Configuración (IC) 
- **Cualquier elemento involucrado en desarrollo** 
- Se conoce info específica para identificarlo 
- Son las cosas que se gestionan en el proyecto
- Puede o no ser atómica (atómica ~= main.c)
### Tipos
- De Proceso
	-> **Generados por el proceso** de desarrollo
	-> Algunos son gestionados durante una parte de la vida
- De Producto
	-> **Propios del producto** SW 
	-> Gestionados por todo el ciclo de vida
## Configuración 
- Conjunto de IC que forman el producto
## Baseline
- Representa estado de config de un conjunto de IC
- Puede tomarse como referencia para siguiente etapa de desarrollo 
- Se establece cuando ICs cumplen n requerimientos
- No necesariamente coincide con un release del SW
## Trazabilidad
- Capacidad de rastrear IC a lo largo de todo el proceso
### Tipos
- Horizontal
	-> Capacidad para trecear los IC a lo largo de todo el proceso ()
- Veritcal 
	-> Capacidad de tracear todos los IC dentro de la misma etapa
## Branching 
- Crear lineas de desarrollo separadas de lineas de producción 
- ...
## Ambiente 
- Entorno de implementación (infraestructura)
- Cada uno tiene un proposito 
