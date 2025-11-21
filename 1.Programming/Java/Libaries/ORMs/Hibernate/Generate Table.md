``` java
public class CreateBD implements WithSimplePersistenceUnit {
	public static void main(String[] args){
		CreateBD instance = new CreateBS();
		instance.crearBD();
	}
	
	public void crearBD(){
		withTransaction(() -> {
		
		})
	}
}
```