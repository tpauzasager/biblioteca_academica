- Persona guarda los atributos de Dirección como su fueran propios
___
```java
@Entity @Table(name"persona")  
class Persona {  
	@Id @GeneratedValue()  
	private Long id;   
	@Embedded  
	private Direccion direccion;  
}
```

```java
@Embeddable  
public class Direccion {  
	@Column  
	private String calle;  
	@Column  
	private String altura;  
}
```
___
![[Pasted image 20241116130652.png]]
