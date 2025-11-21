Funciones
	- Comunicación entre estaciones en el medio compartido 
Caracteristicas
	- Soportar acceso multiple 
	- Trabajar junto a capa MAC
Direccionamiento
	- Usuario LLC -> identificado con SAP (service access point)
# Servicios
Tipos de operación

|                      | Tipo 1                         | Tipo 2                                       | Tipo 3                                                         |
| -------------------- | ------------------------------ | -------------------------------------------- | -------------------------------------------------------------- |
| Orientado a conexión | No                             | Si                                           | No                                                             |
| Confirmación         | No                             | -                                            | Si                                                             |
| Control de           | -                              | Flujo<br>Errores                             | -                                                              |
| Garantiza recepción  | No                             | -                                            | Si                                                             |
| Ventajas             | Sencillo<br>Rapido<br>Barato   | Fiable<br>Para disp simples                  | Garantiza recepción sin conexión previa<br>Rapido<br>Confiable |
| Desventajas          | No fiable<br>Perdidad de datos | Complejo<br>Sobrecarga por mantener conexión | Menos simple que 1ro<br>No tan robusto como 2do                |
# Protocolo 
Basado en HDLC. Diferencias:
- 