- Se crean las siguientes tablas:
	- Una para la clase padre
	- Una por cada clase hija
- Puede estar o no la Columna Discriminador  
- Se usa cuando cada subclase tenga muchos atributos 
- Ventajas:
	- No hay columnas en null
- Desventajas:
	- Se sacrifica performance (porque se deberá hacer join para conseguir la clase completa)
___
```java
@Entity @Table(name="reputacion")  
@Inheritance(strategy = InheritanceType.JOINED)  
public abstract class Reputacion {  
	@Id @GeneratedValue  
	private Integer id  
	@Column(name="nombre")  
	private String nombre  
}  
```

```java
@Entity @Table(name="reputacion_regular")  
public abstract class ReputacionRegular extends Reputacion {  
	@Id @GeneratedValue  
	private Integer id  
	@Column(name="nombre")  
	private String nombre  
}
```
___
![[Pasted image 20241116123802.png]]
