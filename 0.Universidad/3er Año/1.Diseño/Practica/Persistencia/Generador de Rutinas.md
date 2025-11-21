![[Pasted image 20241211163616.png]]

```java
#Persistente
@MappedSuperclass
class Persistente{
	@Id @GeneratedValue
	Long id;
}

#Deportista
@Entity @Table(name="deportista")
class Deportista extends Persistente{
	@Column(name="altura")
	Double altura
	@Column
	String apellido
	@Column
	String nombre
	@Column
	Double pesoInicial
	
	Motivacion motivacionPrinicipal

	@ElementCollection @CollectionTable(name="", joinColumn= @JoinColumn(name="deportista_id"))
	@Column(name="contactos")
	List<String> contactos
}

#Rutina
@Entity @Table

```