![[Pasted image 20241002124642.png]]

# Teoría
1. 
   a. Falso. Si antes de ejecutar la interrupción, la cpu se encuentra ejecutando un KLT u otra interrupción, solo es requerido un cambio de contexto y no de modo
   b. Falso. Al igual que el punto anterior, si la cpu se encuentra ejecutando en modo kernel, no es necesario cambiar de modo para ejecutar la syscall. De igual modo, para ejecutar una syscall, tambien se requiere cambiar de contexto, ya que es el SO el encargado de ejecutar dicha instrución . 
2. 
   Sería mejor utilizar procesos, ya que, cuando estos finalicen, toda la memoria que tenian asignada se liberará. La desventaja sería que es más costoso crear nuevos procesos
3. 
   Si se implementa el jacketing en la situación dada, los ULTs si se aprobecharian de este, aunque no sería tan provechoso a cuando los hilos posean rafagas IO más largas. En conclusión, si podrían llegar a aprobecharlos, pero en la mayoría de los casos, al ser el Queantum corto, podría no llegar a notar una gran diferencia. 
   No, si un proceso tiene al menos uno de sus hijos en ejecución, entonces dicho proceso se encuentra en estado de ejecución. 
4. 
   En el caso de que dos o más hilos accedan a un mismo recurso compartido y que, al menos uno de ellos, lo este modificando, se dice que hay presente una condición de carrera. Esto da lugar a que el proceso en ejecución no sea deterministico y que devuelva valores diferentes para los mismos inputs.
5. 
   Prevensión: Es el que menos overhead tiene, no da lugar a que ocurran deadlocks y es la más restrictiva de todas
   Evasión: Es la que más overhead tiene, no da lugar a que ocurran deadlocks y posee una flexibilidad intermedia.
   Detección: Posee un overhead intermedio, da la posibilidad a que ocurran los deadlocks y posee la mayor flexibilidad de todas