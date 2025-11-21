# One -> One / Many -> One
```java
public class Persona {
	@OneToOne // @ManyToOne
	@JoinColumn(name="libro_id", referencedColumnName="id")
	private Libro libro;
}

public class Libro {
	@Id
	private Long id;
}
```
# One -> Many (list of classes)
## Define column for relation (worst)
``` java
public class Person {
	@OneToMany
	@JoinColumn(name = "persona_id")
	private List<Hair> hairs;
}
```

## Biderectional Relationship
When using  [[zRelationships|Cascade]], put it on one side of the relationship (not in both) 
``` java
public class Person {
	private Long id;
	@OneToMany(mappedBy = "owner")
	private List<Book> books;
}

public class Book {
	@ManyToOne
	@JoinColumn(name = "person_id")
	private Person owner;
}
```
When recursive, its the same 

# Many -> Many 
``` java
public class Children {
	private Long id;
	
	@ManyToMany
	@JoinTable(
		name = "Children_Parent"  //This is default table name
			joinColumns = @JoinColumn(name="children_id", referencedColumnName="id")
		reverseJoinColumns = @JoinColumn(name="parent_id", referencedColumnName="id")
	)
	private List<Parent> parents;
}

public class Parent {
	
	private List<Children> childers;
}
```

___
# Embedded
Location has importar information, but it doesn't require a unique table in BD
``` java
public class Person {
	@Embedded
	private Location location; 
}

@Embeddable
public class Location {
	@Column
	private String street;
	@Column
	private String number;
}
```