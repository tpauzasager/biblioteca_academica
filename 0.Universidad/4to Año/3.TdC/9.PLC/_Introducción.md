# Ladder
![[Pasted image 20251021212200.webp]]
Lectura:
	- Arriba a abajo (pasando del nivel superior al inferior)
	- De izq a derecha
# Compuertas Lógicas
1. AND ![[Pasted image 20251021212538.webp]]
2. OR ![[Pasted image 20251021212550.webp]]
3. Autoretención (una vez activado, no para) ![[Pasted image 20251021212648.webp]]
	Se suele agregar otro pulsador NC (entre Start e Y) para poder cortar el sistema
# Temporizadores
![[Pasted image 20251021212931.webp|200]]
![[Pasted image 20251021220713.webp|400]]
Trg -> Trigger (input)
Par -> Parametrizable
Q -> Salida

Funcionameinto -> Al pasar tanto tiempo con el Trg activo, envía señal (hasta que Trg se desactiva)
## A la desconexión
![[Pasted image 20251021220516.webp|200]]
![[Pasted image 20251021220641.webp|400]]
Funcionamiento -> Recive señal de Trg y comienza a emitir señal. Despues anular Trg y de un momento, deja de emitir señal
# Contador
![[Pasted image 20251021215740.webp]]
R -> ?
Cnt -> Señal que hace sumar el contador
Q -> Salida 

Funcionamiento -> Al recivir señal por Cnt aumenta el contador, al llegar al número indicado, emite señal '1'