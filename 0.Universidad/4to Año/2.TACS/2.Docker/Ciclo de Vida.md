# Build
- Cada comando es una nueva capa 
- Capas jerárquicas (cambiar capa destruye cache de todas las superiores)

Se puede separar la capa de building de la de runtime (para tener contenedor de runtime más liviano)
# Deploy 
- docker pull
Consideraciones con registry
	 - Versionado semántico 
	 - No usar **tag latest** en producción 
# Run
- pull vs push 
- Service discovery <- Orquestador de containers 
# Monitoreo 
- Logs 
- Monitor daemons
- Metricas 
## No gaps 
Monitorear instancia y recursos (HW) a lo largo de todas las capas 
# Producción 
En que?
	- VM
	- Físico 
	- Híbrido 
En donde? 
	- On premise (?)
	- Cloud privado/comercial 
	- Híbridos
