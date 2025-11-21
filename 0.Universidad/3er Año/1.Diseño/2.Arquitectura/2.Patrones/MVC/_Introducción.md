Patrón de arquitectura de SW de interacción que separa la arquitectura en 3 componentes: Modelo, Vista y Controlador

![[Pasted image 20241026193607.png]]
___
# Validación de datos
- Se realiza en cada capa (validación en profundidad)
- Vista -> Campos requeridos y consistnecia (si es núm o letra)
- Controller -> Consistencia, campos requeridos y contra servicio externo (si es que hace falta)
- Modelo -> Validaciones del negocio
___
# Ventajas vs Desventajas
| Ventajas                                                                                   | Desventajas                                                                                                                               |
| ------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| - Buena separación de intereses<br>- Reusabilidad de Vista y Controllers<br>- Flexibilidad | - Mayor complejidad del sistema<br>- No siempre útil en apps con poca interactividad (Vista simple)<br>- Dificil de testar como "un todo" |
