# Definición
Portadora -> Digital
Moduladora -> Analogica
## Tipos

| Tipo | Modifica                                   |
| ---- | ------------------------------------------ |
| PAM  | Amplitud (A)                               |
| PDM  | Ancho pulso ($\tau = d$)                   |
| PPM  | Posición del pulso (con respecto al clock) |
![[Pasted image 20250622164644.webp]]
___
# PCM 
Modulación por Codificación de Impulso
Uso -> Transformar señal Analógica a Digital y modularla

![[Pasted image 20250622165027.webp]]
## Pasos

| Paso                                                                                                                      | Definición                                                                      |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Muestreo                                                                                                                  | $f_{muestreo}>= 2*f_{máx~muestreada}$<br>voz humana -> 256 niveles              |
| Cuantificación                                                                                                            | División de señal analógica en niveles discretos<br>128 niveles para voz humana |
| Codificación Pasaje de niveles a cadena de bits <br>Estandares:<br>    - EU: 7b por muestra<br>	- EEUU: 8b por muestra EU |                                                                                 |

pdh, sdh 
orden digital sincrónico y asincrónico 
tipos de modulación 