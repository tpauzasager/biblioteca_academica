# Logical
``` java
public class PClass { // <--- Generic class to persist --->
	@Id
	@GeneratedValue
	private Long id;
	
	@Column
	private Boolean active = true;   //True when NOT deleted (logycally)
}

public class PClassRepository implements WithSimplePersistenceUnit {
	public void delete(Pclass pclass){
		List<PClass> pclass = this.searchById(id);  //Get all list result from seach
		if(!pclass.isEmpty()){
			PClass pclass1 = pclass[0];    //change 1st result obtained
			pclass1.setActive(false);
			PclassRepository.update(pclass1);
		}
	}
}
```
___
# Physical 
MUST NOT DELETE PHYSICALLY FROM DB (only logically)  
``` java
public class PClassRepository implements WithSimplePersistenceUnit {
	public void delete(Pclass pclass){
		withTransaction(() -> {
			entityManager().remove(pclass);   //Delte to DB
		});
	}
}
```