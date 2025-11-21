# Fourier
#### $$f(t) = \frac{a_o}{2}+\sum_{n=1}^{\infty}{a_n·cos(n\omega t) + b_n·sin(n\omega t)}$$
## Coeficientes
$$a_0=\frac{2}{T}\int_{-T/2}^{T/2}{f(t).dt}$$
$$a_n=\frac{2}{T}\int_{-T/2}^{T/2}{f(t)·cos(n\omega t).dt}$$
$$b_n=\frac{2}{T}\int_{-T/2}^{T/2}{f(t)·sin(n\omega t).dt}$$

## Paridad
$$f(t)~par => \forall n:b_n=0$$
$$f(t)~impar => \forall n:a_n=0$$
