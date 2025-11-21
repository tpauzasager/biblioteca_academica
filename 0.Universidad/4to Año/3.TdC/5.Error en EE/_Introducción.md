![[Pasted image 20250907091320.webp]]

$$G_o(s)=\frac{K.(s^m+...+a_1.s+a_0)}{s^q.(s^n+...+b_1.s+b_0)}$$
q = Tipo de sistema = multiplicidad del polo en origen de coordenadas 

# Error SS

| Error en Tipo | Escalón Unitario                     | Rampa Unitaria                         | Parabola Unitario                        |
| ------------- | ------------------------------------ | -------------------------------------- | ---------------------------------------- |
| $K_i$         | $$K_p=lim_{s\rightarrow 0}(G_0(s))$$ | $$K_v=lim_{s\rightarrow 0}(s.G_0(s))$$ | $$K_a=lim_{s\rightarrow 0}(s^2.G_0(s))$$ |
| **0**         | $$\frac{1}{1+K_p}$$                  | $$\infty$$                             | $$\infty$$                               |
| **1**         | $$0$$                                | $$\frac{1}{K_v}$$                      | $$\infty$$                               |
| **2**         | $$0$$                                | $$0$$                                  | $$\frac{1}{K_a}$$                        |
| **3**         | $$0$$                                | $$0$$                                  | $$0$$                                    |