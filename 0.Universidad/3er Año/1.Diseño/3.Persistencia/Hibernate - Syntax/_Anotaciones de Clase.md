```java

@Entity 
@Table(name="servicio") //Si name = null => name = <nombre de clase>
class Servicio{
	@Id @GeneratedValue
	private Integer id; 
	
	@Column(name="nombre_columna") //Si name = null => name = <nombre atributo>
	private Sring nombre; 
	
	@Column(nullabe=false) //nullabe=false => no puede ser null (default = true)
	private atributoObligatorio

	@OneToMany(mappedBy="usuario") //Indica que acá solo se guardan los datos para poder acceder luego
}
```

MappedBy:
	- El que tenga esto quedará como el que no es dueño de la relación (solo tiene el dato para poder accederlo luego, pero no administra el objeto en la bd)