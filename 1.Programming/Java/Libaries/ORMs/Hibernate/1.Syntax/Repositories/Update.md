``` java
public class PClassRepository implements WithSimplePersistenceUnit {
	public void update(Pclass pclass){
		withTransaction(() -> {
			entityManager().merge(pclass);   //Update to DB
		});
	}
}


//Possible use for update
public void changeValueById(Long id, Integer nValue){
		List<PClass> pclass = this.searchById(id);  //Get all list result from seach
		if(!pclass.isEmpty()){
			PClass pclass1 = pclass[0];    //change 1st result obtained
			pclass1.setValue(nValue);
			PclassRepository.update(pclass1);
		}
	}
```
