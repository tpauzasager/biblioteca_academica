# Definición
Señal Banda Base
	Señal analógica que no sufre ninguna modulación 
	Se usa para LAN

Código de Banda Base
	Se usan para:
		- Eliminar (o disminuir) CC
		- Garantizar sincronismo 
		- Detectarpresencia de señal en la linea 
	Info transmitida por:
		- Estado
			- Niveles
			- Fases o transiciones
		- Cambio de estado
# Clasificación
Según Polaridad:

|          | 0   | 1                    |
| -------- | --- | -------------------- |
| Unipolar | 0   | 1                    |
| Polar    | -1  | 1                    |
| Bipolar  | 0   | $\pm1$ (intercalado) |
Según $\tau$ :

|     | $\tau$ |
| --- | ------ |
| NRZ | = T    |
| RZ  | < T    |

Especiales :

|                        | Polaridad | $\tau$ | Caracteristica                                                                                          | Ejemplo                               |
| ---------------------- | --------- | ------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| AMI                    | Bipolar   | RZ     | -                                                                                                       |                                       |
| HDB-3                  | Bipolar   | NRZ    | '0000' se cambia por:<br>   1 par = R00V<br>   1 impar = 000V<br>R = '1'<br>V = '1' Polaridad invertida | ![[Pasted image 20251204171644.webp]] |
| Manchester             |           |        | '1' => Transición ascendete<br>'0' => Transición descendente                                            |                                       |
| Manchester Diferencial |           |        | Transición siempre a mitad en T/2<br>'0' => Transición en inicio de T                                   | ![[Pasted image 20251204171955.webp]] |
