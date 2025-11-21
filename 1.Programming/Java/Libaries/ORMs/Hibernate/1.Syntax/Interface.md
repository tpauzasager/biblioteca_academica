# State-Full
Need to refactor into an inheritance 
___
# State-Less
i.e. Contact media
``` java
public class StateLessClass implements Interface { ... }

//CONVERTER
@Converter
public class InterfaceConvertor implements AttributeConverter<Interface, String> {
	public String convertToDataBaseColumn(Interface _interface){
		if(_interface == null)
			return null;
		String result = "";
		
		if (_interface instanceof StateLessClass)
			return "StateLessClass"
		//Repeat for each implementation of Interface
	}
	public Interface converToEntityAttribute(String s)
		if(s == null)
			return null;
		
		Interface _interface;
		switch (s){
			case "StateLessClass" -> new StateLessClass();
			//Repeat for each implementation of Interface
			default -> null;
		}
	}
}

@Entity
...
public class OtherClass {
	@Convert(converter = InterfaceConvertor.class)
	private Interface _interface; 
}
```