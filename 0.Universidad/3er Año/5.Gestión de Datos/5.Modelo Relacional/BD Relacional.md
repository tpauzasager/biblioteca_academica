# Reglas Codd
| Regla                              | Descripción                                                                                                     |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Fundación                          | Sistema de gestión de bd funciona usando sólo sus capacidades relacionales                                      |
| Información                        | Información de bd representada como valores en una relación                                                     |
| Acceso garantizado                 | Todos los datos son accesibles recurriendo a: Nombre de relación, valor de PK y nombre columna                  |
| **Valores nulos**                  | DBMS soporta valores nuelos                                                                                     |
| **Diccionario de datos**           | Se cuenta con descripción lógica de los datos almacenados                                                       |
| **Sublenguaje**                    | Puede admitir varios lenguajes                                                                                  |
| Actualización de Vistas            | Vistas actualizables se actualizan por el sistema                                                               |
| Inserción, Actualización y Borrado | Capacidad de manejar la bd                                                                                      |
| **Independencia física y lógica**  | Cambios en representación de almacenamiento o métodos de acceso no deben afectar los programas de aplicación    |
| **Independencia de Integridad**    | Reglas de integridad definidas en sublenguaje de datos y almacenada en Diccionario de Datos, no en aplicaciones |
| Independencia de distribución      | No importa si los datos están físicamente centralizados o distribuidos                                          |
| No subcersión                      | Si sistema soporta lenguaje de bajo nivel, este no puede salter reglas de integridad                            |
___
# Reglas de Integridad
| Regla      | Descripción                                                                                                                               |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Entidades  | Clave primaria de cada tabla no toma valor nulo ni repetido y (si es compuesta) debe tener la menor cantidad de elementos que la componen |
| Relacional | Valor de FK tiene que existir como PK (o ser null) en la otra tabla relacionada                                                           |
| Negocio    | Reglas específicas de cada empresa                                                                                                        |
___
# Diccionario de Datos
(Catálogo del Sistema) Es bd administrada por DBMS. Compuesta por características del modelo relacional