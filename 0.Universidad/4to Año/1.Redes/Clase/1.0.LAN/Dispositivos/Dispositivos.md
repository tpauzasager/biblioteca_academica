# Dominios
De colisión -> Area donde se propaga una colusión 
	- Repetidor/HUB -> Propaga
	- Switch/Puentes -> No propagan
De broadcast -> Area sonde se propagan tramas de broadcast
	- Limitado por routers
___
# Dispositivos

|             | HUB                  | Briedge                  | Switch | Router |
| ----------- | -------------------- | ------------------------ | ------ | ------ |
| Capa        | 1                    | 2                        | 2 o 3  | 3      |
| Descripción | Repetidor multipunto | Union entre 2 estaciones |        |        |
## Switch 
- Capa 2 o 3 (con cap de router)
Tipos de conmutación

| Tipo                     | Funcionamiento                                                           | Monopolización |
| ------------------------ | ------------------------------------------------------------------------ | -------------- |
| **Store &<br>Forward**   | Almacena todo y reenvía                                                  | Si?            |
| **Cut Through**          | Solo lee dir destino (primeros 6B) y reenvía                             |                |
| **Fragment Free**        | Lee primeros 64B (destino, origen, tipo/longitud, tam min de datos, CRC) |                |
| **Adaptive Cut Through** | Adaptativo (Implementación en función de convenciencia)                  |                |
