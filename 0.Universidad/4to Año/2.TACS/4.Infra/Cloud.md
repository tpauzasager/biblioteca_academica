# Definición 
- Modelo de acceso on-demand
- Pool compartido de recursos 
## Caracteristicas

| Caracteristica            | Definición                                                 |
| ------------------------- | ---------------------------------------------------------- |
| On-demand<br>Self-service | Me asigno recursos a utilizar y despues pago por dicho uso |
| Acceso remoto             | Accesible por internet                                     |
| Resource pooling          | Recursos compartidos entre clientes                        |
| Rapid elasticity          | Capacidad de escalar rápidamente                           |
| Measured service          | Se paga únicamente por lo que use                          |
___
# VS
vs Hosting
	- Hosting vos decidis que plan y es fijo 
	- Cloud se puede escalar más dinamicamente

vs Infra Tradicional
	Pros
		- Servicios del proveedor (colas, mails, DBs, etc.)
		- Se puede empezar con bajo coste e ir aumentando 
		- Facil refactorizar 
		- CDN
	Cons
		- No tengo datos en mi poder 
		- Dependencia en agente externo 
		- Costo
		- Me cobra todo lo que hago 
		- Menos flexibilidad (no se puede hacer de todo)
___
# Tipos
![[Pasted image 20251006103340.webp]]


| Tipo | Pros                                                                          | Cons                                                     |
| ---- | ----------------------------------------------------------------------------- | -------------------------------------------------------- |
| IaaS | - Hago lo que quiero<br>- Facil para portar apps<br>- Servicios del proveedor | - Escalabildad manual<br>- Costo licencia<br>-           |
| PaaS | - Autoscalling, Load balancer, Failover                                       | - Requerimientos acotados<br>- App acoplata a plataforma |
| SaaS |                                                                               |                                                          |


