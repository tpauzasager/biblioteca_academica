22 preguntas, Multiple-choice 

Medios físicos
	Retardo no importa (se compensa) en la comunicación. Lo que importa es la diferencia en el retardo. 
	Alambricas
		Cobre (Coaxil, UTP)
		FO
	Inalambrico
		Medios de propagación 
			Tierra (AM) -> Menos que bandas baja (<3MHz); Ondas terrestres; Señales se pueden superponer
			Ionosferica (FM) -> Banda baja ([3;30]MHz, de redioaficionados); Rebota en ionosfera (no es estable => no uso comercial); Gratis de usar; FM100 => Portadora de 100MHz; Dicrimina la que tiene menor amplitud
			Directa -> Banda medio y alta ([30;300]MHz y [300;3000]MHz); Problemas de VH; > 3000MHZ => onda directa   
		Antena tiene que ser (como mín) de $\lambda /2$ de longitud electrica (?) para que transmita toda la energía que recibe, de lo contrario, transforma parte de energía en calor (y no en pot para transmitir)
		Satélite
			Geoestacionario -> 36.000km; vida util depende del combustible disponible (se queda sin => se desecha); Con 3 se cubre todo el mundo 
			De orbita baja -> < 36.000km; Necesito menos pot para transmitir => Antenas más simples; Necesito varios para cubrir una zona durante 24hs  
		Ruido interno del receptor depende de su temperatura
Cableado estructurado 
Multiplexación 
	Agrupación
		PDH - Pleosincronico: 32 canales (30 user; 1 señalización; 1 sincornismo) 
			Niveles (EU)
				$E_1=30*E_0 + 1 señalización + 1 sincronismo$
				$E_N$ -> $E_{N-1}$ . 4.N user; 1 señalización; 1 sincronismo
			Niveles (USA)
				$T_N$ -> 24 x 4.N user; 1 señalización; 1 sincronismo
		SDH (USA) - Sincronico: 
	Métodos
		FDM -> frecuencia
		TDM -> tiempo
		STDM -> tiempo estádisctico (RR - más tiempo al que más info transmite)
		CDM -> código (magia negra )
	$\Delta f \geq \sum_{canales}(f_i)$  => Es transparente (no guarda señal)
	Concentrador
		No cumple que: $\Delta f \geq \sum_{canales}(f_i)$ 
		Guarda señal y la va envíando de a poco 
Modulación (portadora; modulante)
	(analogica; analogica): AM, FM
	(analogica; digital): PSK (fase), ASK (amplitud), FSK (frecuencia) 
	(digital; analogica): PAM (amplitud), PDM (ancho de pulso), PPM (desface del pulso con respecto al clock)
	8QAM -> fase y amplitud => 8 Niveles de info
	PCM
		Pasos
			1. Muestreo = ($f_{muestreo} > MAX(f_{original})$)
			2. Cuantización = pasar valores muestreados a bit/s (EU: 7b por muestra, USA: 8b por muestra) 
			3. Codificación
# Preguntas
Rta = respuesta del profe
Medios físicos
1. Por que puedo transmitir más info a medida que aumento la frecuencia de transmisión? 
	Rta: Mayor frecuencia => Más ciclos por seg => Más ondas por seg=> Más info por seg
2. VH (dijo que usemos 4,14 por curvatura de ondas electromagneticas)
	Rta: $VH=DH_1+DH_2$ ; $DH_1 [km]=4,14·\sqrt{H_1[m]}$    /  H = Altura antena
3. Relación $\lambda = c/f$  /  $c=3.10⁸[m/s]$ 
4. Principal ventaja de satelite de onda baja por sobre los geoestacionarios?
	Rta: Estan más cerca => señal sufre menos atenuación => antenas más simples; Desventaja = Necesito varios para cubrir una zona durante 24hs
Modulación
5. Tipo de señal: Portadora + Moduladora (información) = Modulada 
	Te digo dos y vos decime de que tipo es la que falta 
	Rta: Modulada = Portadora
6. Porque FM es mejor que AM?
	Rta: AM transmite en función de A (amplitud) y este es suceptible al ruido. FM transmite en función de f (frecuencia) la cual no es afectada por el ruido
Multiplexación
7. Diferencia operativa entre FDM y TDM y CMD?
	**Rta: FDM sirve para digital y analogica. FDM y CDM solo funciona para digital** 
8. Porque FDM menos eficiente que TDM, para digital? 
	Rta: Se desperdicia $\Delta f$ en la separación entre las bandas de transmisión (la separación entre B de cada canal) y esto se paga. TDM hay sincronismo 
9. Concentrador?
10. Que es más eficiente PDH o SDH?
	Rta: SDH, porque no hace falta demultiplexar y multiplexar (constantemente) hasta el orden 1 para agregar una comunicación. Se inyecta directamente la trama
___
otras preguntas
1. Porque no se uso PM comercialmente? 
