Puede implementarse en modelo Relacional o Multidimensional
Definición:
	Vistas multidimensionales de cada área del DW
	Ajustada a un aparte del negocio (tiene menor costo creacional y operacional)V
___
# Modelo Estrella
Implementación Data Marts en RDBMS
- Tipos de tabla:

| Hechos                                                                                                                                                                                  | Dimensiones                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Datos concretos de medidas asociadas a un evento<br>**FK de tablas de Dimensiones** <br>Registran eventos con gran nivel de atomicidad (mayor nivel de detalle al modelo transaccional) | Baja cant de registros<br>Registros con gran cant de atributos (para describir datos del hecho) |
