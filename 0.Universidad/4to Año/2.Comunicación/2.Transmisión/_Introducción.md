# Tipo Señales

|                  | Analógica                      | Digital                           |
| ---------------- | ------------------------------ | --------------------------------- |
| Valores          | Continuos                      | Discretos                         |
| Transporte info  | Forma                          | Valor del pulso                   |
| Ruido            | + sensible                     | Sensible, pero se puede regenerar |
| Error            | +                              | -                                 |
| Costo            | -                              | +                                 |
| Medición calidad | S/N                            | BER                               |
| Alcance          | - (amplificación agrega ruido) | +                                 |
Conversión:
	1. Muestreo -> Medición
	2. Cuantificación -> Asignación valor a medición
	3. Codificación -> Asignación valor a bit
___
# Funciones Periódicas

|               |               |
| ------------- | ------------- |
| Periodo       | $T=1/f$<br>   |
| Ancho Pulso   | $\tau$        |
| Longitud Onda | $\lambda=c/f$ |
$f=frecuencia$
$c=3.10^8m/s$ 
## Fourier 
Espectro de magnitud: $|C_n|=A.\tau/T$
Cantidad armonicos: $n=T/\tau$
Ancho banda: $\Delta f = n*f=1/\tau$
___
# Velocidades
Vel. Modulación: $V_m=1/\tau$
Vel. Tx: $V_{Tx}=\sum V_m.log_2(n)$
	n = Cant niveles 
___
# Tipos
Tipos:
	- Simplex: Una dirección 
	- Half Duplex: Bidireccional en mismo canal (Tx o Rx en un instnate)
	- Full Duplex: Dos Canales (Tx y Rx en todo instante)
Modos:

|            | Serie         | Paralelo                                 |
| ---------- | ------------- | ---------------------------------------- |
| Ventaja    | Más distancia | Más velocidad                            |
| Desventaja | Más lento     | Menos distancia (por dispersión de bits) |
Sincronismo:
	- Asincronico
	- Sincronico
		- Por bit -> Identifica a un bit
		- Por caracter -> Identifica grupo de bits
		- Por bloque -> Tiene encabezado
___
# Unidades
W -> dB:
	Potencia -> $P(dB)=10*log_{10}(P(W))$
dB ->W:
	$Potencia -> P(W) = 10^{P(dB)/10}$
