| Nombre                                | Sim           | Unidad    | Definición                                                                                            | Fórmula       |
| ------------------------------------- | ------------- | --------- | ----------------------------------------------------------------------------------------------------- | ------------- |
| **Ancho de pulso**                    | $d$<br>$\tau$ | seg       | Parte del pulso que tiene voltaje<br>A menos d => Hace falta más ancho de banda (pq ruido afecta más) |               |
| **Amplitud de pulso**                 | $A$           | volt      | Voltaje máximo del pulso                                                                              |               |
| **Periodo**                           | $T$           | seg       |                                                                                                       |               |
| **Frecuencia de repetición de pulso** | $FRP$         | PPS<br>Hz | Solo para señales digitales                                                                           | $1/T$         |
| **Frecuencia**                        | f             | Hz        | Para todo (+ generico)                                                                                |               |
| **Velocidad de modulación**           | $V_m$         | baudios   |                                                                                                       | $1/d$         |
| **Valor Eficaz**                      | $V_e$         |           |                                                                                                       |               |
| **Velocidad de tranmisión**           | $V_t$         | bit / seg |                                                                                                       |               |
| **Valor Medio**                       | $V_{med}$     |           |                                                                                                       | $a_0/{\pi}$   |
| **Factor de Forma**                   | FF            |           |                                                                                                       | $V_e/V_{med}$ |
| **Ancho de Banda**                    | $\Delta f$    | Hz        | Rango de frecuencias que se usan para transmitir la señal                                             |               |
| **Velocidad de transferencia**        |               |           | Relación entre cant de bits envíados y el tiempo empleado                                             | $n/t$         |

## Valor Eficaz 
$$\sqrt{\frac{1}{T}\int_0^T{f(t)²·dt}}$$
## Velocidad de Transmisión
$$\sum_i^m{\frac{1}{T_i}.log_2(n_1)}$$
$n_i=\text{cant de posibles valores del la tensión por pulso}$
$m = \text{cantidad de lineas de bits}$
## Valor Medio
$$\frac{1}{T}\int_0^T{f(t).dt}$$




