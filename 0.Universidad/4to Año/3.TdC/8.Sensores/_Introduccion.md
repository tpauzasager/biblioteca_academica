# Proporcional
![[Pasted image 20251008104313.webp]]

|                                         | Control                             | Salida                                       | Modificación de tipo        | Grafico ($e_{(t)}$)                   |
| --------------------------------------- | ----------------------------------- | -------------------------------------------- | --------------------------- | ------------------------------------- |
| proporcional                            | $$K_p$$                             | $$K_p.e_{(t)} == K_p.E(s)$$                  | No                          | ![[Pasted image 20251008110412.webp]] |
| Integral                                | $$K_i/s$$                           | $$K_i\int_0^te_{(t)} == \frac{K_i}{s}.E(s)$$ | Aumenta                     |                                       |
| Proporcional Integral                   | $$K_p+K_i/s$$                       | $$K_p.e_{(t)} + K_i\int_0^te_{(t)}$$<br>     | No <br>(agrega polo y cero) | ![[Pasted image 20251008110327.webp]] |
| Derivativo                              | $$K_d.s$$                           | $$K_d\frac{de}{dt}==K_d.s.E_{(s)}$$          | Disminuye                   |                                       |
| Proporcional Derivativo                 | $$K_p+K_d.s$$                       | $$K_p.e_{(t)}+K_d\frac{de}{dt}$$             | No                          | ![[Pasted image 20251008112521.webp]] |
| Proporcional <br>Integral<br>Derivativo | sumatoria de todas las individuales | sumatoria de todas las individuales          |                             | ![[Pasted image 20251008113256.webp]] |
# Caracteristicas
Proporcional:
	- Integral => $\tau_d=K_p/K_i$
	- Derivativo => $\tau_d=K_d/K_p$

Integral:
	- Salida es proporcional a la suma de errores pasados (respuesta aumenta si van aumentando los errores)
	- Puede volverse inestable 

Derivativo:
	- Tiene una respuesta inicial abrupta (independientemente de la amplitud del error)
	- No responde a un error constante 

Proporcional Integral Derivativo:
	$$Gc_{(s)}=K_p.(\frac{\tau_i.s+1+\tau_i.\tau_d.s²}{\tau_i.s})$$

