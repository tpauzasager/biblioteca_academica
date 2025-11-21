# Lists
## Primitive DataType 
``` java
public class Objeto {
	private Long id;
	
	@ElementCollection
	@CollectionTable(name="obj_caract", joinColumns=@JoinColumn("objeto_id", referencedColumnName="id"))
	@Column
	private List<String> caracteristicas;
}
```
### OrderBy
``` java
@OrderBy("name DES") //Default "id ASC"
private List<PClass> pclass; 
```