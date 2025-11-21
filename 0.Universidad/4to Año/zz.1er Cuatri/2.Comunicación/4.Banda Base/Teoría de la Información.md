# Información del mensaje
### $$I(x_i)=log_b(1/P(x_i))$$
$P(x_i)[equiprobable]=1/\sum\text{posibles valores}$
$b = 2 => I[shannon]$
$b = e => I[nat]$
$b = 10 => I[hartley]$

# Entropía
Representa valor medio de información de todos los mensajes que puede mandar una fuente 
### $$H(x)=\sum_{k=1}^nI_k.P(x_k)$$
$H(x)=[\text{shannon/símbolo}]$
# Tasa de Información 
Representa cant de información de la fuente en cada unidad de tiempo
### $$\Gamma = \frac{H(x)}{\tau}$$
$\Gamma = [\text{shannon/seg}]$
$\tau=\sum P(x_i).T(x_i)$
# Capacidad 
Cantidad de info que canal puede trasnportar por unidad de tiempo
