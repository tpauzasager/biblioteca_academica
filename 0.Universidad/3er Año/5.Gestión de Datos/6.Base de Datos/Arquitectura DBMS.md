# ANSI/SPARC
| Nivel      | Almacenamiento                                       | Funcionalidad                                             |
| ---------- | ---------------------------------------------------- | --------------------------------------------------------- |
| Externo    | Muestra datos relevantes y permitidos a los usuarios | Interacción del usuario con la bd                         |
| Conceptual | Estrucutras de datos y relaciones                    | Analizador sintáctico y semántico<br>Definición de reglas |
| Interno    | Almacenamiento físico de datos y como se accede      |                                                           |

Beneficios
- Vistas de usuario independientes y personalizadas
- Oculta detalle físico de almacenamiento
- Admin es capaz de cambiar estruturas sin afectar vista
- Estructura interna no es afectada por cambios físicos de almacenamiento

# Componentes
| Nombre       | Descripción                                                                                                                                                        |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| IPL          | Initial Program Loader<br>Usado para carga inicial del progra                                                                                                      |
| User Manager | Para manejar perfiles, usuarios y roles<br>Seguridad vertical / horizon                                                                                            |
| File Manager | Administra lógica de archivos del DBMS<br>Creacón/eliminación/Acceso a arch                                                                                        |
| Disk Manager | Administración física de información de la bd<br>Administración/Permisos de usuario<br>Conversión de posición relativa (páginada) a posición real en memoria  oria |
