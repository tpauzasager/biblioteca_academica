Composición:
- Array de bytes (que representa la propia memoria)
- Lista de particiones

Inicialización:
	`make([]byte, TamMemoria)`

# CPU
Retarde de peticiones: 
	Cada una de estas peticiones tiene un tiempo de espera definido en el archivo de configuración
Obtener contexto de ejecución:
	Devolver contexto completo (inclusive base y límite) para el PID-TID pedido
Acutalizar contexto:
	Actualizar registros del CPU para el PID-TID pedido y devolver OK
Obtener instrucción
	Devolver instrucción correspondiente al hilo y PC recibido (pc comienza por elemento cero)
READ_MEM:
	Devolver valor de los primeros 4 bytes a partir del byte envado como dirección física
WRITE_MEM:
	Escribir los primeros 4 bytes enviados a partir del byte enviado como dirección física y responder OK
___
# KERNEL
## Creación de proceso
### Particiones fijas
La lista de particiones vendrá dada archivo de configuración y no se podrá modificar durante la ejecución 
Si no se pudo encontrar hueco: 
	Responder a KERNEL que no se pudo inicializar el proceso
### Particiones dinámicas
Parte de una partición libre (del tamaño total de la memoria) y se irá dividiendo a medida que se vaya pidiendo espacio en memoria

Esquema de asignación:
	- Fist Fit
	- Best Fit  (usar este)
	- Worst Fit

Si no se pudo encontrar hueco:
	Se verifica si el total de huecos libres permite la inclusión del espacio solicitado
	Si el total no es suficiente => Responder a KERNEL que no se pudo inicializar el proceso
	Si el total es suficiente => Realizar compactación de toda la memoria y luego almacenar el espacio requerido