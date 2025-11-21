# BD Multidimensionales 
- Info almacenada de forma dimensional (no relacional) 
- Información de variables determinado por uno o más dimensiones 
- Información puede analizarse por intersección entre dimensiones de la variable
## Dispersión de Datos
Al agregar una nueva dimensión a la bd multidimensional, es probable que muchos valores queden en null
Se evita con Hypercubos y Multicubos
	
Hypercubos
	- Único cubo sin limitación en cant de dimensiones 	
	- Estructura estática 
	- Simplicidad para usuario final
	- Gran velocidad de acceso a info (se almacena de forma contigua)

Multicubos
	- Info dividida en grupos pequeños y densos

Elección Hypercubo vs Multicubo:
	
| Caracteristica | Hypercubo                                                                         | Multcubo                                                                                            |
| -------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Funcionamiento | Único cubo sin limitación de dimensiones                                          | Info dividida en grupos pequeños y densos                                                           |
| Estructura     | Estática                                                                          | Dinámica                                                                                            |
| Ofrece         | Facilidad de comprensión                                                          | Flexibilidad                                                                                        |
| Almacenamiento | Gran efecto de dispersión<br>Velocidad de acceso a info (almacenamiento contiguo) | Eficiencia para datos dispersos y reduce efecto de disperción<br>Usa más espacio que los hypercubos |