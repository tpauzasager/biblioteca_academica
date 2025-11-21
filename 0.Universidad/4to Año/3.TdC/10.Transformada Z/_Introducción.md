Definición 
Pasaje de una serie de muestras a una función (polinomio con factores de $z^{-a}=e^{-a.s}$)
# Teoremas
Valor inicial
	$$f[0] = lim_{t\rightarrow0}f[k]=lim_{z\rightarrow\infty}F(z)$$
Valor final
	$$f[\infty] = lim_{t\rightarrow\infty}f[k]=lim_{z\rightarrow1}(1-z^{-1}).F(z)$$
___
# Retardo 
Retardo Unitario
	(equivalente a realimentación en sistemas cerrados)
	![[Pasted image 20251022101836.webp]] 
	Ecuación de diferencias: $Retardo~Unitario = y[k] = y[k-1]+x[k]$
	(equivalente a ecuación diferencial para sistema discreto)
___
# Transferencia de Pulso
ej:
	$y[k]=y[k-2].a+x[k]$ ==> $Y(z)=a.Y(z).Z^{-2}+X(z)$  ==>  $G(z)=\frac{Y(z)}{X(z)}=\frac{1}{1-a.Z^{-2}}$
___
# Estabilidad
#### $$Z=e^{(\sigma+j.\omega).T}$$ $$Z=\rho.e^{j\omega T}$$
Es estable <=> Las raices tiene modulo <= 1
___
# Conseguir Muestar a partir de F(z)
ej:  $$F(z)=\frac{10Z^{-1}+5z^{-2}}{1-1,2z^{-1}+0,2z^{-2}}$$
1. Dividir polinomio nominador por el denominador
2. El cociente indica los primeros n valores del muestreo 
	Para $a.Z^{-t}$ : a es el valor muestreado y t es el instante de la muestra 
	El cociente te va a quedar como un polinomio con estos valores
___
![[Pasted image 20251029123238.webp]]