Definición:
	Gran vector de bytes (direcciones)
	Tiene dividio el espacio para usuario y para kernel

# MMU 
![[Pasted image 20241025224702.png]]
Unidad de manejor de memoria
- Se encarga de convertir direcciones lógicas (relativas de cada proceso) a físicas (dentro de la memoria prinicipal)
- Está en la CPU
- Las traducciones se realizan en tiempo de ejecución (en etapas de fetch o execute)

# Requerimientos para tradución de memoria

| Requerimiento                  | Descripción                                                                       |
| ------------------------------ | --------------------------------------------------------------------------------- |
| Realocación                    | Los procesos pueden cambiar de posición en la memoria                             |
| Protección y Compartir memoria | Un proceso no puede acceder al espacio de direcciones de otro (sin tener permiso) |
| Organización lógica            | Cómo los procesos acceden a la memoria                                            |
| Organización física            | Como se almacena realmente la memoria                                             |
___
# Comparación entre métodos
![[Pasted image 20241025201334.png]]

