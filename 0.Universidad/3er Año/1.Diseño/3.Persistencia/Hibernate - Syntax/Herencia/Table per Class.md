- Se crean las siguientes tablas:
	- Una clase por cada clase hija 
	- Una tabla para clase padre   <<---????
- Cada tabla tiene atributos de su subclase y de su clase padre
- Ventajas:
	- Buena cuando cada subclase es diferente a nivel negocio 
- Desventajas:
	- No conviene cuando se desean usar polimorficamente
	- Para buscar por Id va a ser necesario buscar en todas las tablas de las subclases (por UNION entre tablas de subclases) ==> Baja performance
___
```java
@Entity  @Inheritance(strategy = InheritanceType.TABLE_PER_CLASS)  
public abstract class Reputacion {
	@Column(name="nombre")
	private Long id;  
	
	@Column(name="nombre")  
	private String nombre;  
}
```

```java
@Entity  @Table(name="reputacion_regular")  
public abstract class ReputacionRegular extends Reputacion {  
	@Column  
	private String algunAtributo;  
}
```
___
![[Pasted image 20241116124426.png]]
