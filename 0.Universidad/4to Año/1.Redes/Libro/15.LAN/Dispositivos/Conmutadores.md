# Concentrador
Definición 
	- HUB
	- Capa 1
	- Elemento activo
	- Retransmisor (re envía trama a todas las estaciones conectadas)
	**- Expande dominio de colisión**
___
# Conmutador capa 2
Definición
	- Switch
	- Capa 2
	- Elemento activo 
	- Retransmisión hacia disp destino 
Caracteristicas
	**- Limita el dominio de colisión**
	**- Permite comunicaciones paralelas entre diferentes pares de dispositovos**
Problemas
	- Sobrecarga de difusión: 
		Todos los disp están en misma red => tramas broadcast se envían a todos
	- Falta de enlaces multiples:
		STP no permite bucles en capa 2 (pq solo puede haber un camino activo entre nodos) => poca tolerancia a fallos
Tipos:

|                     | Almacena      | Desc de almacen                                                    | Ventajas           |
| ------------------- | ------------- | ------------------------------------------------------------------ | ------------------ |
| **Store & Forward** | Todo          |                                                                    | -                  |
| **Cut through**     | 6 primeros b  | Dir MAC destino                                                    | Velocidad          |
| **Fragment Free**   | 64 primeros b | - Dir MAc destino y origen <br>- Tamaño<br>- Longitud min<br>- CRC | Chequeo de errores |
___
# Conmutadores capa 3
## Switch capa 3
Definición 
	- Dispositivo de capa 2 y 3 
	- Gran velocidad (retransmisión por HW)
## Router
Definición
	- Routers
	- No cuenta como conmutador
Caracteristicas 
	- Divide red en subredes => Restringe broadcast
	- Se permiten multiples caminos entre subredes (por algoritmos de enrutamiento)
Desventajas
	- Menos velocidad que un switch (de capa 3) (retransmisión por SW)
