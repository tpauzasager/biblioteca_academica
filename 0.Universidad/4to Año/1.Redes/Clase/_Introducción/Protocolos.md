# Normas IEE
![[Pasted image 20250826102845.webp]]
___
PDU -> Unidad de datos protocolar  
# Protocolos
**Definición** 
	- Conjunto de reglas y procedimientos para regular comunicación entre dispositivos 
	- Provee HEADER y TRAILER
**Permite**
	- Intercambio info entre mismas capas y diferentes sistemas 
	- Interoperabilida entre sistemas 
**Funciones** (control de...)
	- Flujo de datos
	- Actividad en canal
	- Segmentación y ensamblado -> armar y desarmar PDU
	- Transparencia -> Agregar datos de protocolo para no afectar datos orginales 
	- Encapsulamiento 
	- Sincronismo
	- Conexión
	- Entrega en orden 
	- Direccionamiento -> Sondeo y selección 
	- Muliplexación -> Varias conexiones en mismo vinculo 
	- Servicios de transmisión
# Caracteristicas
**Arquitectura**
	- Monoliticos -> Único protocolo
	- Estructurados -> Conjunto de protocolos organizados por capas
**Tipo de enlace-red**
	- Directo -> P2P
	- Indirecto -> Nodos como intermediarios
**Jerarquía**
	- Simétrico -> P2P
	- Asimétrico -> Cliente-Servidor (jerárquico)
**Normalización**
	- Normalizado -> Mismo proto para todas las comunicaciones
	- Desnormalizado -> 1 proto por cada comunicación
# Servicios

|                | Con conexión        | Sin conexión               |
| -------------- | ------------------- | -------------------------- |
| Monopolio      | Con y Sin           | Sin                        |
| Orden llegada  | Con                 | Sin                        |
| Encaminamiento | Tubo (unico camino) | Independiente por cada PDU |
| Transferencia  | Sin errores         | Mejor intento              |
| Modo operación | Circuito virtual    | Datagrama                  |
# Sondeo y Selección 
**Definición** -> Control de transmisiones en canal compartido 

EP(Estación primaria), ES(Estación secundaria)
**Sondeo**   
	- EP gobierna canal compartido
	- EP sondea las ES y detecta si tiene que mandar 
	- Si canal libre => permite comunicación de la ES y continua sondeo 
**Selección**
	- EP tiene mensaje previamente enviado por ES y lo envía al al destino correspondiente 