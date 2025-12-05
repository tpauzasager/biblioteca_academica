# Onda Electromagnética 
OEM
	$\lambda=c/f$
# Espectro Electromagnético 

| Banda de Propagación | $\Delta f [Hz]$ | Uso                           |
| -------------------- | --------------- | ----------------------------- |
| ELF                  | 300 - 3000      |                               |
| VLF                  | 3K - 30K        |                               |
| LF                   | 30K - 300K      | Sonar                         |
| MF                   | 300K - 3000K    | AM                            |
| HF                   | 3M - 30M        | Radiocomunicación             |
| VHF                  | 30M - 300M      | FM                            |
| UHF                  | 300M - 3000M    | Wifi 2.4<br>Radiocomunicación |
| SHF                  | 3G - 30G        | Wifi 5.8<br>Satélite          |
| EHF                  | 30G - 300G      | Satélite                      |
Por espacio libre:
	- HF, VHF, UHF
# Medios Físicos
## Caracteristicas
Impedancia
	- Absoluta -> Igual a Imp en 1u. de distancia
	- Característica -> En función de prop fisicas del cable (para distancia $\infty$)
Efecto pelicular 
	A mayor frecuencia => Mayor atenuación 
	Pq onda tiene a viajar por periferia del conductor
## Tipos
Par Telefónico
	- Par de cobre -> 1 Tx y 1 Rx
	- Multipar -> Varios pares

Par trenzado
	- Está balanceado
	- Trenzado para evitar diafonía
	- Categoría UTP en función del trenzado

Coaxil
	Composición
		1. Conductor central 
		2. Aislante que propaga el OEM (lleva la información)
		3. Malla protectora (conectada a tierra), para aislar
		4. Cubierta exterior
	- No es balanceado

Radio
	Bandas de operación:
		- HF, VHF, UHF, SHF

Antenas
	- Emite OEM por el espacio libre 
	Modos propagación
		Ionosférica
			- Refracción en capa más alta de atmósfera
		Terrestre
			- Onda de superficie (viaja por tierra)
			- Onda directa (linea directa hacia la otra antena)
	Calculo distancia entre antenas: $$D[Km]=3,16\sqrt{H[m]}$$
	Componentes antena
		- Plato reflector (sólido o enrejado)
		- Radomo (cubierta protectora para antenas)
		- Iluminador (recibe y genera OEM)
	Pérdida en espacio libre: $$L=32,4+20.log(d[km])+20.log(f[Mhz])$$

Satelites ![[Pasted image 20251205084006.webp]]
	$f_1\neq f_2$ : Para evitar bloqueo 
	$f_1 > f_2$ : Para que mayor atenuación esté de bajada, porque es más facil agregar ganancia en tierra
	Tipos satélite
		- Orbita baja -> (150;450)km
		- Orbita media -> (6000; 15000)km
		- Geoestacionarios -> 35000km
	Bandas de Operación (UIT)
		![[Pasted image 20251205084927.webp|500]]
		