# Nodo Oculto 
1. Nodo A y C no se escuchan (por distancia u obstrucción)
2. Ambos se quieren comunicar con B y, como no se escuchan mutuamente, detectan que el canal esta libre
3. Ambos intentan comunicarse al mismo tiempo y resulta en colisión en B

Soluciones
- Utilizar RST/CTS 
# Nodo Expuesto 
1. A transmite a B
2. C quiere escucha a A y quiere transmitir a D
3. C no detecta a B => No transmite a D (pq piensa que el canal está ocupado)

Soluciones
- Utilizar RST/CTS 