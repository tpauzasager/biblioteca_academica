Multi Protocol Label Switching
# Definición
- Mejora IP sobre ATM
- Para hacer tuneles 
- Para acelerar encaminamiento de paquetes 
- Integra Nivel 2 (conmutación rápida) y 3 (control de enrutamiento)
- Soporta cualquier tipo de tráfico 

Objetivos:
	- Mejorar congestión 
	- Delay (predecible y no predecible)
	- Perdida de paquete 
	- Acelerar routeo 
	- Camino optimo 

Caracteristicas
	- Trabaja con etiquetas 
	- Puede trabajar con cualquier otro protocolo de Nivel 2 

Componentes
	- LSR (Label Swithing Router) 
		- Router que trabaja con etiquetas
		- Tipos
			- Acceso -> Agregan o quitan etiquetas
			- Interno -> Leen y enrutan en función de las etiquetas
	- Etiqueta
		- Identifica un FEC
		- Hay jerarquía de etiquetas (más de una por paquete)
	- FEC (Forwarding equivalence Class)
		- Agrupación de paquetes que comparten atributos (dirección, destino, VPN)
		- Se asigna cuando entra a la red 
		- Paquetes del mismo FEC van por mismo LSP
	- LSP (Label Switch Path)
		- Ruta de 1+ LSRs
		- Por donde van los paqueteso

PDU
![[Pasted image 20251102212004.webp|600]]
TTL -> Tipo to live en redes IP
S -> Stack (indica si hay otra etiqueta de diferente jerarquia)
Exp -> Clase de servicio

Protocolos de ruteo:
	- Se siguen usando los comunes (RIP, IGP, etc)
	- Se agregan unos específicos para los LSRs

