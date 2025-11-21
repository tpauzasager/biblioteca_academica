Definición:
	Colección de datos historicos, que permite la integración y filtrado de información de varias fuentes 
	Esta info es procesada y analizada desde diferentes puntos de vista 
___
# Funcionalidades
| Función          | Descripción                                                                                                            |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Acceso a fuentes | Mapeo, Integración y muestreo de datos fuente                                                                          |
| Carga            | Extracción, Depuración, Conversión, Carga                                                                              |
| Almacenamiento   | Puede implementarse en varias BD simlutaneamente<br>Pueden usarse RDBM o MDDBM (multidimensional)                      |
| Consultas        | Data Mining<br>Simulación de negocios: Herramienta spara comprobar impacto en transformaciones en ambiente de negocios |
___
# Migración de datos
Trasladar datos desde sistema origen hasta stage del DW
Solo se mueven datos relevantes
Incluye datos referenciales (cliente) y transaccionales (ventas) 
___
# Carateristicas

| Caracteristica      | Descripción                                                                     |
| ------------------- | ------------------------------------------------------------------------------- |
| Orientado a sujetos | A sujetos mayores de la organización (para operaciones y funciones no clasicas) |
| Integrado           | Los datos se integran antes de llegar al DW (desde modelo transaccional)        |
| Temático            | Solo se añaden datos necesarios para el análisis                                |
| Variante en tiempo  |                                                                                 |
| Simple de manejar   | Operaciones: Carga inicial, acceso a datos (no necesita update)                 |
| No es volátil       | No se admite modificación en los datos                                          |
___
Objetivos:
	Conservación de datos de aplicaciones OLTP antes de ser procesados en ambiente OLAP 

