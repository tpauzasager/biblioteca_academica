- Atributos de la superclase son persistidos en la tabla de las clases hijas ([Embedded]) 
- La superclase no se considera como entidad (no tiene tabla propia)
- ORM no puede recuperar instancia de clase padre (porque no la considera una clase)
___
```java
@MappedSuperclass  
public abstract class Persistente {  
	@Id  @GeneratedValue  
	private Long id;  
  
	@Column(name="activo")  
	private Boolean activo  
}
```

```java 
#CLASE HIJA
@Entity  @Table(name="consumidor")  
public class Consumidor extends Persistente {  
	@Column(name="nombre")  
	private String nombre  
	
	@Column(name="apellido")  
	private String apellido  
}
```
___
![[Pasted image 20241116123632.png]]