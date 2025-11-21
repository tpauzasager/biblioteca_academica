# Cache for SELECT's
Hibernate has a two level cache. Whenever you try to recover objects (only by Id) from DB, it first checks his cache then it does whatever query is left required  

# List Recovering
``` java
@OneToMany(fetch = FetchType.LAZY) //When recoverted, list won't be transfer to RAM (just when explicitly used)
			   //= FetchType.EAGER //Always downloads the full lists (even if not used)
private List<Integer> list; 
--
List<Class> classes = classRepository.searchAll()   //Up to here, no list's where downloaded into RAM
this.classes[0].getList();   //Just up to here, that list was download into the RAM
```
if lists already in CACHE ==> It downloads them anyways  