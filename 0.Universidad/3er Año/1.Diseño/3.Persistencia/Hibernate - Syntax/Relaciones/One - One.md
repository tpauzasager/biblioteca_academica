```java
@Entity @Table
public class Empleado{
	@Id @GeneratedValue
	private Integer id;

	@OneToOne
	@JoinColumn(name="perfil_id", referencedColumnName="id")
	private Perfil perfil;
}
```

```java
@Entity @Table(name = "perfil")  
public class Perfil {  
  @Id @GeneratedValue  
  private Integer id;  
}
```