___ 
# Protocolo IP
Definición
	- Unidad básica para transferencia de datos
	- **No orientado a la conexión y no confiable** (si ocurre error => algún prot de capa superior se encarga de arreglarlo)

Direccionamiento -> Dirección IP (manejada por SW)

Servicio -> **Mejor esfuerzo** (llegar por el camino de menor esfuerzo)

Uso
	- Toma datos de nivel superior (TCP o UDP) y los inserta en internet
	- Usa ICMP (corrección de errores)

Datagramas 
	- Independientes entre si
	- Si tamaño datagrama excede tam de trama de capa 2 => Fragmentación (lo hace el router)
## Datagrama
![[Pasted image 20250902090258.webp|700]]

| Campo                          | Descripción                                                                                                                                                | Tam (b) |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
|                                | **----1ra Palabra-----**                                                                                                                                   |         |
| Versión                        | De la IP {4,5,6}                                                                                                                                           | 4       |
| Long header                    | Determina longitud de encabezado [20;60]B (mín 20 pq header fijo tiene tam 20B)                                                                            | 4       |
| Tipo Servicio                  | 6b -> Servicios diferenciados<br>2b -> Notificación de congestión                                                                                          | 8       |
| Long total                     | Medido en octetos, incluye todo                                                                                                                            | 16      |
|                                | **----2da Palabra----**                                                                                                                                    |         |
| Identificación                 | ID del databrama (fragmentación)                                                                                                                           | 32      |
| Bandera                        | Controlar fragmentación (dando info) [Más fragmentación, no fragmentar]                                                                                    |         |
| Desplazamiento<br>de fragmento | Indica el desplazamiento utilizado para el mecanimso para fragmentar                                                                                       | 13      |
| <br>                           | **----3ra Palabra-----**                                                                                                                                   |         |
| Tiempo de vida                 | Limite de saltos que el datagrama tiene permitido permanecer en internet<br>IP funciona por inundación en la red => T vida impide que se expanda sin parar | 8       |
| Protocolo                      | Identifica el protocolo de capa superior (TCP -> 6 o UDP -> 17)                                                                                            | 8       |
| Check Sum                      | Detección de errores en header (solo en header)                                                                                                            | 16      |
|                                | **----4ra Palabra-----**                                                                                                                                   |         |
| Opciones + Relleno             | por si acaso                                                                                                                                               |         |
# Data extra 
- Router guarda tabla sw direcciones ip para todos sus puertos (LAN y WAN)
- Dir IP identifica dispositivo en la red => Si disp cambia de red => Hay que cambiar dir IP 

