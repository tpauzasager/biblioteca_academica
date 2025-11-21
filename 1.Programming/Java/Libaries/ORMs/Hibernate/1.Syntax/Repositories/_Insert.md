``` java
@NoArgsConstructor    //Required for Hibernate 
public class PClass { // <--- Generic class to persist --->
	@Id
	@GeneratedValue
	private Long id;
	
	@Column
	private Boolean active = true;   //True when NOT deleted (logycally)
}


public class PClassRepository implements WithSimplePersistenceUnit {
	//1st Option
	public void save(PClass pclass){
		entityManager.persist(pclase);  // entityManager prepares INSERT sentence, but doesn't execute it
	}

	//2nd Option (executes transactios directly from repository, more encapsulation, less logic in controller)
	public void save(PClass pclass){
		withTransaction(() -> {
			entityManager.persist(pclase); 	// No need to open and commit transactions
		})
	}
}


public class RepositoryController implements WithSimplePersistenceUnit {
	public static void main(String[] args) {
	
	//1st Option 
	public void guardarPClass(PClass pclass){
		beginTransaction();
		PClassRepository.save(pclass);
		commitTransaction();            // Must use transactions to implement changes in DB
	}
	
	//2nd Option 
	public void guardarPClass(PClass pclass){ 
		withTransaction(() -> {
			PClassRepository.save(pclass);	// No need to open and commit transactions
		})
	}
} 
```