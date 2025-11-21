# Definición 
DevOps -> Fusión entre Desarrollo y Operación (up time)
Conjunto de prácticas para reducir _time to market_, garantizando calidad

CI/CD -> Pipe line para desarrollas, deployear, testear e implementar cambios 

Integración Continua
	- Detección temprana de errores (testing, building, linting)
	- Detección problemas seguridad 
	- Estandarización de buildings 
	- Feedback 
	
Continuous D
	- Maneja ambientes de desplegue
	- Deployment -> con intervención 
	- Delivery -> sin intervención 

Principios
	- Reducir silos (trabajos aislados con intereses distintos) en la organización 
	- Aceptar el fallo como algo normal 
		Reducir ATTR (avarage time to recovery) y ATTF (avarage time to fail)
	- Mayor frencuencia de deploy (cambios más graduales)
	- Automatización 
		Deploys, Migraciones / Mantenimiento, Enlarges / Shrinks
	- Medir todo
___
# IaC
Infrastructure as Code

Definición 
- Para definir arquitectura como código
- Objetivos
	- Abstracción 
	- Reproducible 
	- Versionado 
	- Declarativo vs Imperativo 
	- Vendor lock in 
___
# Git Branching
Definición 
	Se le da una funcionalidad a cada branch (main, test, features)
	Para estandarizar flujo de trabajo 

Ventajas
	- Estandarización (aumento gobernanza)
	- Mejora flujo de trabajo 
	- Flujos específicos por cada tipo de branch 
## Gitflow
Tipos e branch
	- Feature (de desarrollo)
	- Hotfix (se puede integrar directo a master)
	- Release (para mergear las features)
	- Estable (codigo productivo)
Backports -> Cuando mergeo un hotfix, se actuliza tambien las diferentes ramas 
___
# Orquestador de Containers
Para
- Menjar ciclo de vida de los containers 
- Networking -> Trabajo colaborativo entre muchos servicios 
- Escalamiento -> Cantidad de instancias de cada servidor 
- Asignación de recursos
- Rolling updates -> Implementar nuevas versiones en los contenedores 
- Portabilidad
## Kubernetes
- Open Source 
- Declarativo -> Se define que se quiere (Estado deseado y depues la herramienta hace lo posible para cumplirlo)
- Container runtime 
Componentes
- Nodos (master -> Gestión ; Workers -> Containers de produción)
- Kubernetes api -> Esta en master. Se usa para gestionar kubernetes (dar instrucción y observabilidad)
- ETCD -> 
- Scheduler -> 
- Controllers -> Para comparar estado real con el deseado de los workers
- Objects -> 
___
# GitOps
Definición
- Git como fuente de verdad 
- Versionado 
- Automatización de cambios 
- Separción aplicación - manifiesto 

Tener un componente que escucha los cambios en el repositorio y los implementa automaticamente 


