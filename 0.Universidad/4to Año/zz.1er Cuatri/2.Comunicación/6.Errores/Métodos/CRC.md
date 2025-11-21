Código de redundancia cíclica 

$M(x) = \text{Mensaje}$
$G(x) = \text{Generador}$
$R(x) = \text{Resto}$
$T(x) = M(x) + R(x) = \text{Pol transmitido}$

# Caracteristicas
- Se emplea en detección por HW (pq se usa XOR para división)
# Metodología
1. Definir M(x) y G(x)
2. Dividir M(x) por G(x) y obtener R(x)
3. Transmitir T(x) = M(x) + R(x)