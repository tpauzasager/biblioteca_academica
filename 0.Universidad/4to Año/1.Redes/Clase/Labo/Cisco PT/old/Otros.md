Cancelar comando erroneo
	- Ctrl + Shift + 6

Ejecutar comandos en modo anterior
	- do <comando/> 
	ej: Si estoy en modo config y quiero hacer un show, uso do para no tener que hacer exit antes y pasar a modo sudo

Comando **Show**
	- show running-config -> muestra configuración actual 
	- show startup-config -> muestra configuración default 
	- show vlan brief -> lista todas las vlans creadas en ese switch

# Cables 
Directo:
	- Switch - PC
	- Switch - Router 
Curzado:
	- Switch - Switch
	- Router - Router 
	- PC - Router

# Borrar configuración 
**no** <configuración a borrar/> 

# Seguridad 
- Agregar contraseña a sudo 
	-> config terminal (ya desde sudo)
	-> enable secret <contraseña>
- Agregar constraseña a CLI
	-> (en modo config) line con 0
	-> password <contraseña> 
	-> login 
- Limitar puerto de switch por MAC de dispositivo
	-> (config-if)# switchport port-security 
	-> (config-if)# switchport port-security  mac-address <mac address del dispositivo/> 
	