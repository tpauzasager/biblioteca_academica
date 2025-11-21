# Single Table
This will generate one table with the following columns:
	| cero | first | second | tipo_clase |
``` java
@Entity
@Inheritance(strategy = InheritanceType.SINGLE_TABLE)
// Column to difference between each subclass type
@DiscriminatorColumn(name = "tipo_clase") // "TYPE" is default column name
public abstract class SuperClass {
	@Column
	private String cero;
	
	public void Method()
}

@Entity
@DiscriminatorValue("FirstSubclass")
public class SubclassOne implements SuperClass{
	@Column
	private String first;
	@Override
	public void Method(){ ... }
}
@Entity
@DiscriminatorValue("SecondSubclass")
public class SubclassOne implements SuperClass{
	@Column
	private String second;
	@Override
	public void Method(){ ... }
}
```
___
# Joined
``` java
@Entity
@Inheritance(strategy = InheritanceType.JOINED)
@DiscriminatorColumn(name = "tipo_clase") 
public abstract class SuperClass {
	@Id
	@GeneratedValue(strategy = GenerationType.TABLE) //Must use type TABLE 
	@Column
	private String cero;
	
	public void Method()
}

@Entity
@DiscriminatorValue("FirstSubclass")
@Table(name = "firstSubclass")
public class SubclassOne implements SuperClass{
	@Column
	private String first;
	@Override
	public void Method(){ ... }
}

@Entity
@DiscriminatorValue("SecondSubclass")
@Table(name = "secondSubclass")
public class SubclassTwo implements SuperClass{
	@Column
	private String second;
	@Override
	public void Method(){ ... }
}
```
