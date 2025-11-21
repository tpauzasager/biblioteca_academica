# Definición 
- Transmisión de datos analógicos y digitales por medio analógico
- Se usa en WIFI y Bluetooth
![[Pasted image 20250919095520.webp]]
# Funcionamiento
1. Señal codificada a analógica con AB pequeño 
2. Señal modulada entra a generador de pseudo ruido (por código expansor) lo que desplaza el AB (manteniendo tamaño)
3. Receptor utiliza decodificador para componer señal 
# Ventajas
- Inmunidad al ruido / interferencias 
- Cifrado de señal 
- Varios usuario pueden usar mismo AB en simultaneo 
# Desventajas
 - Perdida de eficiencia espectral ($V_{Tx} / \Delta f$) 
# Tipos
## Salto de frecuencias 
FH
- Cada paquete enviado respeta el AB fijo 
- Cada paquete es enviado con el AB desplazado (en la dimensión de la frecuencia), pero con el mismo AB
![[Pasted image 20250919100341.webp]]
## Secuencia directa
DS
- Cada bit se encuentra subdividido en otros bit de menor $\tau$, por lo que se incremente el AB
- Se mantiene $V_t$ y disminuye 
![[Pasted image 20250919100539.webp]]
