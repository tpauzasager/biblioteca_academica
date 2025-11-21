# Bidireccional
Agregar el `mappedBy="self_nombre_tabla"` para indicar ...
```java
@Entity @Table(name="servicio")
class Servicio{
	@Id @GeneratedValue
	private Integer id;

	@OneToMany(mappedBy="servicio") //Para cuando la relación es bidireccional
	private List<Tarea> tareas;
}
```

```java
@Entity @Table
class Tarea{
	@Id @GeneratedValue
	private Integer id;

	@ManyToOne
	@JoinColumn(name"servicio_id", referencedColumnName="id")
	private Servicio servicio;	
}
```
___
# Unidireccional

```java
@Entity @Table(name="servicio")
class Servicio{
	@Id @GeneratedValue
	private Integer id;

	@OneToMany
	@JoinColumn(name="tarea_id", referencedColumnName="id")
	private List<Tarea> tareas;
}
```


```java
@Entity @Table
class Tarea{
	@Id @GeneratedValue
	private Integer id;
}
```
