Se usa **solo** cuando $F(x)$ es muy dificil de calcular 

# Pasos
1. Se calcula un $\vec{R}=(r_x,r_y)$
2. Si $\vec{R} >= (r_x,f(r_x))$ (si el punto está sobre o debajo de la curva f)=> Se **rechaza** el $r_x$ y se vuelve a generar otro 
## Eficiencia del método
$$e=\frac{1}{M.(b-a)}$$
- Para mejorar la eficiencia:
	- Hacer $M = Max(f(x))$

# Diagrama de flujo
![[Pasted image 20250415142545.webp]]