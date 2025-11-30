PV = Valor ganado previsto hasta el momento 
EV = Valor de lo realizado hasta el momento (PV real)
AC = Costo de lo realizado hasta el momento (lo que me costó el EV)

| Nombre                                       | Acrónimo | Formula                                                                   | Definición                                                                     |
| -------------------------------------------- | -------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| Variación de costos                          | CV       | $EV-AC$                                                                   |                                                                                |
| Variación de cronograma                      | SV       | $EV-PV$                                                                   |                                                                                |
| Índice de desempeño de cronograma            | SPI      | $EV/PV$                                                                   | Desempeño del trabajo realizado hasta el momento                               |
| Índice de desempeño de costos                | CPI      | $EV/AC$                                                                   | Cantidad gastado hasta el momento (independientemente del avance del proyecto) |
| Variación a la Conclusión                    | VAC      | $BAC-EAC$                                                                 | Diferencia entre el costo total planificado y real                             |
| Desempeño de costos requerido para finalizar | TCPI     | 1. $(BAC-EV)/(BAC-AC)$<br>2. Si hay nuevo presupuesto $(BAC-EV)/(EAC-AC)$ |                                                                                |
## Estado del proyecto
![[Pasted image 20250612103407.webp]]
CPI < 1 => Gasté más de lo que planifique 
CPI > 1 => Gasté menos de lo planificado 

SPI < 1 => Hice menos de lo que planifique 
SPI > 1 => Con la plata gastada hice más de lo que esperaba
# EAC

| Desempeño        | Definición                                                                                                              | Formula                    |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------- | -------------------------- |
| Tipico           | Se mantiene performance de costos observada hasta el momento                                                            | $BAC/CPI$                  |
| Atípico          | Performance de costos observada hasta el momento fue excepcional => no se mantiene, se usa la planificada originalmente | $AC+BAC-EV$                |
| Cambio de des    | Se cambia performance de costos observada hasta el momento                                                              | $AC +(BAC-EV)/CPI_{nuevo}$ |
| Nueva estimación | Mala estimación incial                                                                                                  | $AC+Nueava~Estiación$      |
$CPI_{nuevo}=(BAC-EV)/(BAC-AC)=CPI.SPI$
___
# Comparación con Ágil
![[Pasted image 20250612105041.webp|500]]![[Pasted image 20250612105054.webp|500]] Se usa ágil para para proporcionar info en EVM
