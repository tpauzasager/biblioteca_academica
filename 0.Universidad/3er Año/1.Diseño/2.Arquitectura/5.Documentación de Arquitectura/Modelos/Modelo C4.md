![[Pasted image 20241105093019.png]]

Objetivo:
	- Aliviar brecha modelo-código
	- Permite comunicar arquitectura en función de niveles de detalle
	- Niveles:
		 1. Contexto
		 2. Contenedores
		 3. Componenetes
		 4. Código
___
# Contexto
- Imagen genérica de sistema e interacción con exterior
- Especificar sistemas externos y sus interacciones con nuestro sistema
- Sistema modelado como caja negra (solo interesa conecciones externas)
- Permite identificar usuarios finales 
- **Diagrama de Contexto** 
___
# Contenedores
- Contenedor -> Cualquier entidad que ejecuta código o almacena datos
- Ej: Aplicación/Servicio web, App de escritorio, Base de datos, etc.
___
# Componentes
- **Detalla un contenedor particular** manteniendo contexto 
- Cada componente tiene un grupo de funcionalidades
- Muestra responsabilidad del componente y detalla su implementación 
___
# Código
- Muestra **detalle de implementación**
- Diagrama de Clases / Datos / Secuencia / etc...