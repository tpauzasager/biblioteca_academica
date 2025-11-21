- Se crea una tabla que contiene:
	- Atributos de clase padre
	- Todos los atributos de cada clase hija
	- **Columna Discriminador**, para que ORM identifique que tipo de clase debe instanciar
- Ventajas: 
	- Gran performance (solo se deberá consultar una única tabla)
- Desventajas:
	- Muchas columnas quedan en null
___
```java
@Entity @Table(name="reputacion")  
@Inheritance(strategy = InheritanceType.SINGLE_TABLE)  
@DiscriminatorColumn(name="tipo")  
public abstract class Reputacion {  
	@Id @GeneratedValue  
	private Long id;  
	
	@Column(name="nombre")  
	private String nombre  
}
```

```java
@Entity  
@DiscriminatorValue("mala")  
public abstract class ReputacionMala extends Reputacion {
  @Column(name="atributoDeMala")  
  private String atributoDeMala  
}  

@Entity  
@DiscriminatorValue("regular")  
public abstract class ReputacionRegular extends Reputacion {  
}
```
___
![[Pasted image 20241116123614.png]]
