# 8
```cpp
sem_entrada = 0; 
sem_salida = 0;
p_libres = 10; 
puede_pasar = 0;
pistasLibres = 1; <--Mutex;

### AVIÓN
mantenimiento()
s(sem_entrada)
w(puede_pasar)
despegar()
s(sem_salida)

volar()

s(sem_entrada)
w(puede_pasar)
aterrizar()
s(sem_salida)

### ENTRADA
w(sem_entrada)
w(p_disponible)
otorgarUnaPista()
s(puede_pasar)

w(pistasLibres)
pistasLibres--
log(pistasLibres)
s(pistasLibres)

### SALIDA
w(sem_salida)
liberarUnaPista()
s(p_libres)

w(pistasLibres)
pistasLibres++
log(pistasLibres)
s(pistasLibres)
```
___
# 9
```cpp 

sem_jugador[5]={1,0,0,0,0}
sem_puede_patear = 0
sem_arbitro = 0
sem_puede_validar = 0
sem_validado = 0
sem_pelota_pateada = 0
### ÁRBITRO

w(arbitro)
w(arbitro)
dar_orden()
s(puede_patear)

w(puede_validar)
validar_tiro()
s(validado)
s(validado)

### JUGADOR (5 instancias)

w(jugador[actual()])
posicionarse()
s(arbitro)

w(puede_patear)
patear()
s(pelota_pateada)

s(validado)
if(GOL==TRUE){
	festejar()
} else { lamentarse() }

s(jugador[siguiente()])

### ARQUERO

posicionarse()
s(arbitro)

w(pelota_pateada)
atajar()
s(puede_validar)

s(validado)
if(GOL==FALSE){
	festejar()
}else{ lamentarse() }
```
___ 
# 10 
```cpp 

sem_hijo_disponible = 50
mutex_logger = 1
sem_hay_padre = 0

########

w(hijo_disponible)
pid = fork();
if (pid < 0) {
	w(logger)
	log(Error)
	s(logger)
	s(hijo_disponible)
} else if (pid == 0){
	w(hay_padre)
	w(logger)
	log("Y yo soy el hijo")
	s(logger)

	realizarTarea()
	// Finaliza proceso hijo
	s(hijo_disponible)
	exit(0)
} else { // Padre
	w(logger)
	log(pid + "soy tu padre")
	s(logger)
	s(hay_padre)
}
```