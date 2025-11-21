- En datagrama IP, es posible que el campo de Header Length tenga valores menores a 20? 
No, porque header fijo (que siempre lo tiene) tiene tamaño 20 => como mín HL toma valor de 20

![[Pasted image 20250902093616.webp]]

- En el datagrama IP, viaja el identificador de red? 
No, viaja la dir IP entera, que ahí tambien está incluido el identificador de red 

- Las mascaras por donde viajan?
Las máscaras no viajan, se almacenan en los dispositivos de configuración (ej router)

- Si tengo IP = 200.10.20.30
Mascara default (clase C): 255.255.255.0
Mascara sin clase (formato CIDR): /24


- TCP es con conexión y IP es sin conexión. Como es posible?
Son protocolos de capas diferentes, así que si se pueden dar 

- Vector distancia para una configuración de routers