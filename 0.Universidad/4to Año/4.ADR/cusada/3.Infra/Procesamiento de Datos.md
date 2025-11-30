# Infraestructura 
Requerimientos:
	- Confiabilidad 
	- Rendimiento 
	- Sustentabilidad económica 
Elementos:
	- Unidad de procesamiento 
		- Confiable 
		- Disponible 
		- Tolerancia a fallos (poder seguir funcionando cuando hay fallas)
		- Escalable 
		- Compatible 
		- Administración remota 
		- Mantenimiento en caliente 
	- U almacenamiento 
	- Sist comunicaciones 
	- SW procesamiento 
	- SW base 
# Mainframe vs Supercumputadora 

|                 | MainFrame                                             | Supercomputadora                                        |
| --------------- | ----------------------------------------------------- | ------------------------------------------------------- |
| Función         | Servidor de proposito gral (bd, atender requests, IO) | Realizar calculos complejos                             |
| Velocidad       | Millones de instrucciones por segundo                 | Miles de millone por segundo                            |
| SO              | Varios                                                | Linux                                                   |
| Trabajo         | División por clusters de mainframes y almacenamiento  | Parallel computing (muchos CPUs conectados en paralelo) |
| Consumo energía |                                                       |                                                         |
| Memoria         | hasta 10Tb                                            | Hasta x000 Tb                                           |
___
# Servidores 
Tower
	- Son rackeables
	- Van en armarios donde meto o saco unidades 
Blade 
	- Se compacta todo lo requerido por la cpu en una unidad y se la agrega al rack 
	- Solo procesamiento
Hiperconvergentes
	- Procesamiento y almacenamiento 
___
SO: Permite gestion de HW
# Virtualización 
Definición:
- Permite administrar HW compartido como si fuera parte propia
- Da capa de abstracción con respecto a las aplicaciónes para poder administrarlas en diferentes dispositivos, como si fueran uno solo 
- Permite aumentar HW en caliente (mientras funciona)

Orquestación:
	SW para simplificar config y administración de componentes arquitectonicos 
___
# Cluster de Procesamiento 
Definición:
	- Grupo de recursos de procesamiento individuales trabajando en conjunto 
	- Unidades de procesamiento dedicadas 
Objetivo:
	- Agrupar subsistemas de procesamiento 
	- Facilitar escalabiildad y disponibildad 

Ejemplo:
![[0.Universidad/4to Año/1.Redes/Clase/99.Img/Pasted image 20250814094245.webp|500]]
- Sistema que requiere gran velocidad de lectura, pero no de escritura 
- Cuando llega request de escritura -> Servidor central replica en instancias del servidor de aplicación
- Cuando llega request de lectura -> Load balancer elige de que servidor de aplicación leer 
___
# Grid Computing 
Definición 
	- Conjunto de elementoes heterogéneos trabajando en conjutno 
	- Hace uso de potencia residual de computadora conectada a la red (ej: utorrent)
Caracteristicas
	- Descentralizado 
	- Diversidad de reursos y dinamismo 
	- Administración descentralizada
