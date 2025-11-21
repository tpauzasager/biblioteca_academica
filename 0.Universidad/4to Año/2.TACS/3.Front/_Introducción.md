# Definiciones
Cliente HTTP
	- Tipos
		Liviano
		Pesado

FrontEnd
	- Sistemas de cara al usuario 
___
# Performance 
Métricas 
	- TTFB (Time to First Byte): Desde comienzo de request hasta primer Byte de response
	![[Pasted image 20250912191532.webp|600]]
		Amarillo -> Servidor        ;         Celeste -> Browser(DOM)
	- LCP (Largest Contentful Paint): T para renderizar imagen más grande visible dentro de la ventana
	- FMP (First Meaningful Paint): ?
___
# Pasos para el Renderizado 
1. ![[Pasted image 20250912191802.webp|500]]
	Se procesa el HTML + CSS
2. Carga asincrona de los scripts de JS ![[Pasted image 20250912191956.webp|500]]
	1ra Request es 100% sincrona => Para que esta carga inicial no tarde tanto, se suele patear las cosas menos relevantes con JS asincrono (que se ejecuta luego de la carga inicial)	
	Otras formas de mejorar:
		- CSS en otro archivo separado del HTML
		- ...
3. Lighthouse 
	- Herramienta de tools de chrome 
	- Da reporte exhaustivo sobre aspectos de performance 
___
# Dinamismo 
## Ajax
JavaScript asíncono + XML
Métodos:
	- AJAX
	- JQuery (callback)
	- Promises
	- Async-await (promises con syntax sugar)
___
# JS Frameworks
## ReactJS
Funcionamiento
	- Genera Virual DOM
	- Modifica VDOM y despues actualiza las diferencias con el DOM real 
