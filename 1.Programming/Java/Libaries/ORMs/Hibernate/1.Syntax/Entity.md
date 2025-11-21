# Common Class
```java
import javax.persistence.*;

@Entity 
@Table(name = "clases_persistidas") //Not necessary, just for table configuration
public class Clase extense Persistente {
	@Column(name = "nombre_atributo", nullable = false)
	private Integer atributo;
}

@MappedSuperclass
public abstract class Persistente {
	@ID
	@GeneratedValue(strategy = GenerationType.TABLE)
	private Long id;
	
	@Column   //default name == activo
	private Bollean activo;
	@Column(name = "fechaAlta", columnDefinition = "DATE")
	private LocalDate fechaAlta
}
```
___
# Ignored Attributes 
``` java
@Transient
private Integer num; //This attribute won't be persisted (used for testing while coding) 
```
___
# Primary Key
``` java
public class PersistedClass {
	@Id
	@GeneratedValue(strategy = GenerationType.TABLE)     // One set of Id's for each table 
 //							 = GenerationType.AUTO       // Managed by Hibernate by dedicated table for Id's
 //							 = GenerationType.IDENTITY   // Managed entirely by SQL
 //							 = GenerationType.SEQUENCE   // BD posgres
	 private Long id; 
}
```