# Introducción 
Estados de la salida:
1. Transitorio 
	-> Tiempo hasta que se estabiliza el sistema ante un cambio en la entrada
	-> No hay error
2. Estable 
	-> Hay error

___
# Estabilidad
Define como responde un sistema ante una entrada finita
- Valor inicial finito y Salida tendiendo al infinito => **Inestable**
## Teoremas
$lim_{t\rightarrow 0}f(t) = lim_{s\rightarrow \infty} s.F(s)$  
$lim_{t\rightarrow \infty}f(t) = lim_{s\rightarrow 0} s.F(s)$  
___
# Respuesta al Sistema
$\tau$ -> Tiempo caracteristico 
Gss -> Respuesta en estado estable
## 1er Orden
**Escalonada**:
- $\theta_o = \theta_i.Gss.(1-e^{-t/\tau})$
- $\tau = (1-e^{-1})=0,632$
- ED: $\theta_i.Gss=\tau.\frac{d\theta_o}{dt}+\theta_o$

**Impulso**:
- $\theta_o=\theta_i.Gss.e^{-t/\tau}/\tau$ 
- $\tau=e^{-1}=0,368$ 
- ED: $\theta_i.Gss=\tau.\frac{d\theta_o}{dt}+\theta_o.\delta(t)$

**Escalonada**:
- $\theta_o(t)=\theta_i.Gss.(t+\tau.e^{-t/\tau}-\tau)$ => $\theta_o(s)=\theta_i.Gss(1/s^2+\frac{\tau}{(s+1/\tau)}-\tau/s)$
- ED: $\theta_i.Gss=\tau.\frac{d\theta_o}{dt}+\theta_o.t$
