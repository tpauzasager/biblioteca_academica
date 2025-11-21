![[Pasted image 20251026171545.webp]]
# Definición 
Los polos de la función de transferencia determinan el comportamiento de la respuesta transitoria 


$$G(s).H(s) = \frac{K.\sum(s-z_i)}{\sum(s-p_i)} = \text{Función de transferencia de lazo abierto}$$
$$1 + G(s).H(s) = 0 => -K = \frac{\sum(s-p_i)}{\sum(s-z_i)}$$
# Construcción de Lugar de Raíces 
1. Cant de ramas = cant de polos (de G.H)
2. Todo el eje real forma parte del luegar de raíces 
3. K cambia de signo cada vez que pasa por un polo o cero (simple y por el eje real) 
4. Punto existe en el LGR <=> a la derecha tiene una cant impar de (polos + ceros)
5. Puntos de comienzo y fin de las ramas
	$\frac{-1}{K}=\frac{\sum(s-z_i)}{\sum(s-p_i)}$
	i. s -> $z_i$ => $K$ -> $\pm \infty$ => Lugar de raíces comienza y termina en los ceros impropios (en el infinito)
	ii. s-> $p_i$ =>  $K$ -> $\pm 0$ => Lugar de raíces pasan por polos

6. Cantidad asíntotas = Angulo de las ramas (con respecto al eje real positivo) 
	$$B = \frac{180°}{p_t-z_t}$$
	$p_t =$ Cant de polos
	$z_t =$ Cant de ceros

7. Centroide (punto de intersección entre asintotas)
	$$\phi = \frac{\sum(p_i)-\sum(z_i)}{p_t-z_t}$$

8. Punto de desprendimiento (a partir de cuando las raíces empiezan a ser complejas)
	Valores de S que cumplen:
		$$\frac{-dK}{ds} = 0$$

9. Angulo entre tangente de ramas y horizontal de cero o polo complejo conjugado
	$$\sum{\alpha _i} - \sum{\phi_i} + \beta = 180°$$ 
	$\beta$ = Angulo formado entre la tangente del lugar de reaices y la horizontal

10. Intersección del lugar de caíces con eje imaginario
	Aplicar Routh y buscar los K que anulan a la 1ra columna

11. Graficar 
	Angulo de inclinación para cada rama:
		K > 0 : 
			$\beta_i = \frac{180°.(2.r+1)}{p_t-z_t}$ 
		K < 0 :
			$\beta_i = \frac{180°.(2.r)}{p_t-z_t}$ 
___
# Determinar si punto existe en ubicación de raíz
Por condición de ang
	$$\sum{p_i} - \sum{z_i} + \beta = 180°$$ 
