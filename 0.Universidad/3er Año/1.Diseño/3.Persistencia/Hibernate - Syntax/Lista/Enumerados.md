```java
@Entity  
@Table(name = "persona")  
public class Persona {  
	@Id @GeneratedValue(strategy = GenerationType.IDENTITY)  
	private Long id;  
	
	@Enumerated(EnumType.STRING)  
	@ElementCollection()  
	@CollectionTable(name = "persona_estado",  
		joinColumns = @JoinColumn(name = "persona_id",referencedColumnName="id")  
		)  
	@Column(name = "estado")  
	private List<EstadoPersona> estados;  
}
```
![[Pasted image 20241116130105.png]]
