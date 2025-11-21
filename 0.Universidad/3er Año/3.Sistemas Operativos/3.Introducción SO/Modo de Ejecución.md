- Usuario normal no puede ejecutar a nivel kernel, en necesario pasar a modo kernel para interactuar con SO (las syscalls se encargan de eso)
# Cambio de Modo
- User -> Kernel  &&  Kernel -> User 
## Por Interrupción
## Por Fast Syscalls
- Mediante instrucciones especificas 
- Se ahorra tiempo de overhead al no requerir un cambio completo del contexto para usar las syscalls ([[0.Universidad/3er Año/3.Sistemas Operativos/999.Aclaraciones|Aclaración 1]])

# Anillo de Protección
![[Pasted image 20240828212451.png]]
