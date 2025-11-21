![[Pasted image 20241105093428.png]]

Definición:
	- Filosofía de diseño de software
	- Refiere a organización del código en componentes (módulos) separados y cómo se relacionan entre sí
	- Diseñar app con bajo acoplamiento y alta cohesión 
	- Capas concéntricas
	- Capas internas no deben conocer capas externas (flujo obligatorio de afuera a dentro)
___
# Capas
## Entidades
- Soporta reglas de negocios
- Críticas para la funcionalidad de una app
- Independientes de cualquier otro elemento 
- No conocen nada sobre otras capas
## Casos de Uso
- Acciones que usuario puede realizar 
- Interactúan con entidades 
- No determina apariencia del sistema para usuario (puede no tener UI)
- Describen relgas que gobiernan interacciones entre usuario y entidades
## Adaptadores de Interfaz
- Conexión entre exterior y casos de uso y entidades
- Traductores entre dominio e infraestructura 
## Infraestructura 
- Representa agentes externos (UI, BD, etc.)
- Capa más volátil (porque elementos tienden a cambiar)