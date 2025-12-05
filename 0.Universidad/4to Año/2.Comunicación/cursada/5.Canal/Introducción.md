# Definición
- Vinculo por donde ocurre la comunicación entre terminales
- Objetivo: Trasnferencia máxima de info libre de errores (con menor cant)
- Ideal == Sin ruido ni errores 
# Caracteristicas

| Físico                  | De Información                          |
| ----------------------- | --------------------------------------- |
| Resistencia             | Técnicas de codificación                |
| Inductancia             | Redundancia                             |
| Capacitancia            | Integridad de info (control de errores) |
| Atenuación y distorsión |                                         |
| Ruido                   |                                         |
# Calidad del canal 
- Analógico -> Depende del S/N
- Digital -> Depende de BER (bit error rate) 
___
# Fenómenos que afectan al canal
## Atenuación 
- Disnimución de intensidad de señal 
- No deforma la señal (solo baja V)
- **Mayor frecuencia = Mayor atenuación**

## Distorsión 
- Deformación de señal original 
- Por efectos reactivos del canal 
### Tipos

| Por              | Definición                                       | Solución                         |
| ---------------- | ------------------------------------------------ | -------------------------------- |
| Atenuación       | En cada frecuencia, hay una atenuación diferente | Agregar atenuación (ecualizador) |
| Retarde de grupo | Frecuencias no se propagan a misma velocidad     | Agregar retardo (ecualizador)    |
## Ruido
- Perturbación que se suma a la señal 
### Tipos

| Nombre                   | Definición                                                       |
| ------------------------ | ---------------------------------------------------------------- |
| Térmico                  | Ruido blanco<br>Por agitación térmica de electrones              |
| Crosstalk                | Acoplamiento inductivo entre canales físicos                     |
| Impulsivo                | A intervalos irregulares y de corta duración (por meteorológico) |
| Intermodulación          |                                                                  |
| Factor de amplificadores | Amplificadores agregar ruido                                     |
