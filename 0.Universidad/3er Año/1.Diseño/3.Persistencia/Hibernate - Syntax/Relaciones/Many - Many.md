# Tabla intermedia simple
```java
@Entity @Table  
public class Producto {  
  @Id @GeneratedValue  
  private Long id;  
  
  @ManyToMany  
  @JoinTable(  
    name = "producto_categoria",
    joinColumns = @JoinColumn(name = "producto_id", referencedColumnName = "id"),  
    inverseJoinColumns = @JoinColumn(name = "categoria_id", referencedColumnName = "id")  
  )  
    private Set<Categoria> categorias = new HashSet<>();  
}
```

![[Pasted image 20241116114814.png]]
___
# Tabla con datos adicionales
```java
@Entity @Table  
public class Alumno {  
	@Id  
	@GeneratedValue  
	private Integer id;  
  
	@Column  
	private String nombre;  
  
	@OneToMany(mappedBy = "alumno")  
	private Set<CursadaMateria> cursadas;  
}
``` 

```java
@Entity @Table  
public class Materia {  
	@Id  @GeneratedValue  
	Integer id;  
     
	@Column  
	String nombre;  
}
```

```java
@Entity @Table  
public class CursadaMateria {  
    @Id @GeneratedValue  
    private Integer id;  
  
    @ManyToOne  
    private Alumno alumno;  
  
    @ManyToOne  
    private Materia materia;  
  
	//Información adicional de la relación many-many
    private double notaPrimerParcial;  
}
```