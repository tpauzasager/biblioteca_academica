E = constante dieléctrica del aislante
D = Diametro conductor externo 
d = Diametro conductor interno 

| Propiedad                     | Unidad     | Definición                                                                                                                 | Formula                                       |
| ----------------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| **Capacidad<br>**             | [pF/m]     |                                                                                                                            | $$C=\frac{24,16·E}{log(D/d)}$$                |
| **Inductancia<br>**           | [$\mu$H/m] |                                                                                                                            | $$L= 0,463·log(D/d)+0,522.10⁻6$$              |
| **Impedancia caracteristica** | [Ohms]     | - Resistencia al paso de energía de corriente alterna<br>- No depende de la frecuencia de señal (solo de caract del cable) | $$Z_0=\frac{138}{E} · log(D/d) = \sqrt{L/C}$$ |
# Efecto pelicular
- A mayor frecuencia, mayor es la atenuación 
- Porque frecuencias altas viajas por periferia del conductor
# Impedancia vs Impedancia característica

| Impedancia                                            | Impedancia Característica                                                       |
| ----------------------------------------------------- | ------------------------------------------------------------------------------- |
| Resistencia que se opone al paso de corriente alterna | Impedancia para cable con longitud infinita                                     |
| Depende de frecuencia (por efecto pelicular)          | No depende de frecuencia <br>Depende de caracteristicas constructivas del cable |
# Adaptación de Imepdancia característica
Para que toda la potencia del transmisor continue por el canal de comunicación, en necesario que las impedancias características ($Z_0$) estén bien adaptadas (sean similares)
