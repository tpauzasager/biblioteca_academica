All data definitions missing comes from [[1.Programming/Java/Libaries/ORMs/Hibernate/1.Syntax/Repositories/_Insert]]
# By Id
``` java
public class PClassRepository implements WithSimplePersistenceUnit {
	
	public Optional<PClass> seachById(Long id){
		return Optional.ofNullable(entityManager().find(PClass.class, id)); //If id exists => Optional = object found
																			//If doesn't ==> Optional = Null
	}
}

//Check if returned Optinal is not null
//Optional<PClass> possiblePClass = PClassRepository.searchById(123L);
//possiblePClass.isPresent() == True  =>  It found smth
//possiblePClass.get()  Returns class PClass (without the wrapper)

//possiblePClass.isPresent() != possiblePClass.isEmpty()
//It also works: possiblePClass.get() != null  //for checking if it found smt
```
___
# By attribute
``` java
public class PClassRepository implements WithSimplePersistenceUnit {
	
	public List<PClass> seachByValue(Integer sValue){
		return entityManager()
			.createQuery("from" + PClas.class.getName() + "where value =: sValue")
			.setParameter("sValue", sValue)
			.getListResult();  //List should be used bc value coud not be unic => query coud return multiple results
	}
}
```
___
# All Table
``` java
public class PClassRepository implements WithSimplePersistenceUnit {
	
	public List<PClass> searchAll(){
		return entityManager()
			.createQuery("from" + PClass.class.getName() + "where active =: sActive")   //Checks if active
			.setParameter("sActive", true)
			.getResultList();
	}
} 
```