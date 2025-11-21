- Se utiliza un converter 
___
```java
@Entity @Table  
public class Cliente {  
	@Convert(converter = TipoCliente.class)  
	@Column(name = "tipo")  
	private TipoCliente tipo;  
}
```

```java
# CONVERTER
@Converter(autoApply = true)  
public class TipoClienteConverter implements AttributeConverter<TipoCliente, String>{
    @Override  
    public String convertToDatabaseColumn(TipoCliente tipo) {  
        if (tipo instanceof ClienteNormal ) {  
            return "normal";  
        } else if (tipo instanceof ClientePremium ) {  
            return "premium";  
        }  
        return null;  
    }  
    @Override  
    public TipoCliente convertToEntityAttribute(String dbData) {  
        if ("normal".equals(dbData)) {  
            return new ClienteNormal();  
        } else if ("premium".equals(dbData)) {  
            return new ClientePremium();  
        }  
        return null;  
    }  
}
```

```java
# INTERFAZ
public interface TipoCliente {  
    public void darRecompensa(Cliente cliente);  
}  
  
public class ClienteNormal implements TipoCliente {  
    @Override  
    public void darRecompensa(Cliente cliente) {} 
}  
  
public class ClientePremium implements TipoCliente {  
    @Override  
    public void darRecompensa(Cliente cliente) {}
}
```