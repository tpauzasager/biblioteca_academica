# BD
Definición:
	Conjunto de datos interrelacionados que se ajustan a una serie de modelos preestablecidos que recogen información almacenada sin redundancia. Finalidad de servir a aplicación e independiente a la misma

# DBMS
Data Base Managemnt System
Definición:
	SW encargado de gestionar la BD
	Proporciona mecanismos de acceso a los datos (a traves del SO) 

# Propiedade

| Nombre           | Descripción                                                                                                            |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Atomicidad       | Las transacciones son atómicas, por lo que todas sus operaciones se realizan al completo o no se realiza ningúna       |
| Consistencia<br> | Cualquier transacción lleva la bd de estado valido a otro valido (cumple con reglas de integridad)                     |
| Aislamiento      | Operaciones no puede afectar a otras <br>Cuando y como los cambios se hacen visibles                                   |
| Durabilidad      | Las operaciones son persistidas y no se pueden deshacer <br>Preservar información del objeto y poder recuperarlo luego |
# Funciones
| Función                                | Descripción                                                                                |
| -------------------------------------- | ------------------------------------------------------------------------------------------ |
| Diccionario de Datos                   | Conjunto de tablas que define cada objeto                                                  |
| Control de seguridad                   |                                                                                            |
| Integridad                             | De entidad (PK), Referencial (FK) y De dominio<br>Exactitud y validez de datos almacenados |
| Consistencia                           |                                                                                            |
| Mecanismo de resguardo de restauración | Bakup y restore                                                                            |
| Facilidad de auditorias                |                                                                                            |
| Logs de sistema                        |                                                                                            |
___
# Almacenamiento de Archivos
Archivo:
	Hace falta identificar contenido para poder tipificarlo y administrarlo
Header:
	Conjunto de caracteres que se coloca al inicio y permite definir contenido del resto del archivo
Extensión:
	Relacionada con tipología y aplicación que debe abrirlo