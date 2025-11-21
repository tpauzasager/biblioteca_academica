``` java
@NoArgsConstructor
public class Person extends Persistence {
	@ManyToOne(cascade = {CascadeType.PERSIST, CascadeType.MERGE}) //If persis a Person with new Book's => First persists those Book's then persists the Person
	@JoinColumn(name = "owner_id")
	List<Book> books;
}
```