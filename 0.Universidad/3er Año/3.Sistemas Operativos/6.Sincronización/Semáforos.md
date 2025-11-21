- Estructura del SO, accesible a través de syscalls 
```go
SEM = 1 
wait(SEM)
//Sección Crítica
signal(SEM)
```

Pseudo código de como maneja el SO los semáforos
``` go
//Con espera activa
wait (sem){
	while(sem == 0); 
	sem--;
}

signal (sem){
	sem++;
}

//Con Bloqueo
wait(S){
	valor--;
	if(valor < 0)
		block(); //Bloquea este hilo (porque ya hay otro ejecutandose)
}
signal(S){
	valor++;
	if(valor <= 0 )
		wakeup(pid); //Despierta a algun hilo bloqueado
}
```
___
# Con Espera Activa 
- No tiene bloqueo, espera iterando en el while
- Pueden tener valor negativo (en algún momento de ejecución)
Es mejor usar con espera activa cuando:
- Hay más de una CPU
- La SC es pequeña
# Sin Espera Activa
- Tiene bloqueo al detectar que el semáforo está bloqueado 
- Nunca van a tener valor negativo

___
# Valor del Semáforo
- > 0 ==> Cant de slots libres para acceder al recurso
- < 0 ==> Cant de hilos bloqueados, que esperan acceder al recurso
___
# Tipos de uso
## Mutex
- Para solucionar problema de exclusión mutua
- Siempre inicializa en 1 
## Contadores
- Permite acceso al recurso de N hilos 
## Binarios
- Garantiza orden de ejecución 
- Representa dos estado (libre, ocupado)
## Productor Consumidor 
Combinación entre Mutex y Binario
___
# Herencia de Prioridades 
## Problema
1. Hilo A (de baja prioridad) hace uso de un recurso y lo bloquea
2. Hilo B (de alta prioridad) necesita usar el mismo recurso, pero, al estar bloqueado, se bloquea el hilo B
3. Hilo C (de media prioridad) bloquea al hilo A (porque es de mayor prioridad)
- Como resultado el hilo B queda bloqueado más tiempo del necesario, por culpa de un hilo de menor prioridad (el C)
## Resolución 
- El planificador iguala el nivel (aumentando) de prioridad de los hilos que utilicen un recurso compartido y este este resguardado por un mutex, para que no se genere un deadlock. 