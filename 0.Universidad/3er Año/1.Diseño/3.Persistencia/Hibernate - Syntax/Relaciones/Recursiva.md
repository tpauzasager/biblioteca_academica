# Tabla Intermedia
```java
@Entity 
@Table(name = "Empleado")
class Empleado {
	@Id @GeneratedValue
	private Integer id;
	
	@ManyToMany
	private List<Empleado> subordinados;
}
```
![[Pasted image 20241116115636.png]]
___
# Atributo Padre
```java
@Entity  
@Table(name = "Empleado")  
class Empleado {
	@Id @GeneratedValue  
	private Integer id;  

	@OneToMany  
	@JoinColumn(name="jefe_id", referencedColumnName = "id")  
	private List<Empleado> subordinados;  
}
```
![[Pasted image 20241116115653.png]]
