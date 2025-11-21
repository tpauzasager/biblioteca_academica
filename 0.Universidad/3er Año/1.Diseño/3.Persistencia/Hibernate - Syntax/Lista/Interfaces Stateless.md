```java
# PERSONA
	@ElementCollection  
	@CollectionTable(name = "ElementoDefensor")  
	@Convert(converter = ElementoDefensorConverter.class)  
	@Column(name = "elemento")  
	private List<ElementoDefensor> elementosDefensores;
```
```java
# CONVERTER
@Converter(autoApply = true)  
public class ElementoDefensorConverter implements AttributeConverter<ElementoDefensor, String> {  
  
public String convertToDatabaseColumn(ElementoDefensor elementoDefensor) {  
	return elementoDefensor.getClass().getSimpleName();  
}  
	public ElementoDefensor convertToEntityAttribute(String dbData) {  
		switch (dbData) {  
			case "Arco": return new Arco();  
			case "Escudo": return new Escudo();  
			default: throw new IllegalArgumentException("Unknown" + dbData);  
		}  
}}
```