# Acceso a Config
Desde PC (en misma red) conectado al AP:
	- Web Browser 
	- http:// [AP-address] 
	- Insertar usr y password (default -> admin, admin)
# Seguridad 
Ya dentro de la conafig del AP
1. Desactivar SSID
	Wireless -> Basic Wireless Settings -> SSID Broadcast: -> Disabled	
2. WLAN
	Wireless -> Wireless Security:
		Security Mode = WPA2 Personal
		Excryuption = AES
		Passphrase = [password]

# DHCP
Asigna automaticamente dir IPs y evita conflictos 
En config del AP:
	Setup -> Basic Setup -> Internet Setup -> Internet Connection type = DHCP

___
# Modo Router
Para que se comunique con otras LANs
En AP config
1. Setup -> Internet Setup -> Internet Connection type = Static IP
	Internet IP Address = Red dentro de la LAN 
	Default Gateway = IP del router con el que se van a conectar para salir de la LAN
2. Setup -> Network Setup: 
	IP address = ?
	Activar DHCP