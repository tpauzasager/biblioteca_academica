# Aseguramiento de calidad 
- Revisión y auditoría de productos y actividades 
- Para verificar cumplimineto de procedimientos y estándares 
# Prueba de SW
- Probar == Ejecutar componente para producir fallas 
- **Prueba exitosa si ecuentra fallas**
# Incidente de Testing
- Ocurrencia de evento 
- Durante ejecución de una prueba de SW
- No toda incidencia es una falla

| Nombre       | Definición                                                                      | Genera                 |
| ------------ | ------------------------------------------------------------------------------- | ---------------------- |
| Equivocación | Acción humana que produce resultado incorrecto                                  | 1+ defectos            |
| Defecto      | Proceso definido incorrectamente                                                | 0+ fallas              |
| Falla        | Resultado de ejecución incorrecto<br>Al haber diferencia con resultado esperado | depende de 1+ defectos |
___
# Casos vs Condiciones de prueba
Condiciones de prueba
	-> Descripción de situaciones que quieren probarse 
	-> Proceso creativo
Casos de prueba
	-> Instancia de condiciones
	-> Lotes de datos para determinar condición de prueba
	-> Proceso laborioso
## Criterio de selección 
- Condición para seleccionar conjunto de casos de prueba 
## Partición 
- Todos los posibles casos de prueba son divididos en clases 
- Clases equivalentes <=> Detectan mismos defectos 
- Se cubre todas las pruebas haciendo ejemplos de clases equivalentes
- Exito de testing depende de las particiones 
## Depuración 
- Eliminación de defectos en SW
- Puede ser fuente de más defectos 
- 