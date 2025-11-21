```java
@ElementCollection  
@CollectionTable(name = "persona_emails", joinColumns = @JoinColumn(name = "persona_id"))  
@Column(name = "email")  
private List<String> emails;
```
![[Pasted image 20241116125741.png]]
