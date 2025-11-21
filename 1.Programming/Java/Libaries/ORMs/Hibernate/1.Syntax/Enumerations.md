# Enumeration
## Simple
``` java
public class Persona {
	@Enumerated(EnumType.STRING) //Convert to string
	private TipoDocumento tipoDocumento;
}
```
## Java DataType (converter)
To personalize enums from java
``` java
public class Compra {
	@Convert(converter = DiaSemanaConverter.class)
	private DayOfWeek dia; 
}

public class DiaSemanaConverter implements AttributeConverter<DayOfWeek, String> {
	@Override 
	public String convertToDatabaseColumn(DayOfWeek dia){
		switch (dia){
			case MONDAY -> return "Lunes";
			case TUESDAY -> return "Martes";
			...
			default -> return "";
		}
	}
	
	@Override
	public DayOfWeek converToEntityAttribute(String s){
		switch (s){
		case "Lunes" -> return DayOfWeek.MONDAY;
		...
		default -> null;
		}
	}
}
```