- Valores del enum enlistados (desde 0 en adelante) y se guarda dicho valor
```java
@Enumerated (EnumType.ORDINAL)  
@Column(name="rolEnComunidad",nullable = false)  
private RolEnLaComunidad rolEnLaComunidad;
```