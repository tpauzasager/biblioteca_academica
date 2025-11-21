# En Memoria
- Memoria RAM volátil, pero las hay persistentes (PMem) 
- Mayormente usada para test del sistema
___
# En Archivos
- Guardar estado del sistema en uno/s archivos, que luego pueden ser recuperador, para que el sistema pueda recuperar estado de ejecución 
- Formatos:
	- XML / CSV / Ancho Fijo / JSON / otros...
___
# Pre-valencia 
- Guarda estado en memoria principal y regularmente genera **SNAPSHOTS**, para no perder por completo los datos
- Puede manejar transacciones
- No hay transformación de datos (son persistidos en el formato que el sistema entiende) ==> Mayor performance y no interoperabilidad
- La memoria tiene que soportar todo el sistema 
___
# Ortogonal
- ?
___
# Base de Datos
- En una o varias BD
- Datos persistidos requieren transformación 
- Se maximiza interoperabilidad 
- BD tiene herramientas de recuperación e integridad 
- Data Mapper (hibernate) o Active Record
## BD orientada a objetos
- Atada a un lenguaje de programación particular 
- No es necesario transformar los datos 
- No hay interoperabilidad 
## BD no-sql