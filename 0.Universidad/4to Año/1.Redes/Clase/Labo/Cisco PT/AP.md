# Bridge
En GUI del AP:
## DCHP
Setup/Basic Setup: 
	Internet Connection type = DHCP
	Router IP = ?
	DHCP Server Settings:
		DHCP Server = Enable
		Start IP address = ...
		Maximum number = ...
## Wireless
Wireless/Basic Wireless Settings:
	Network Name (SSID) = [AP_name]
	SSID Broadcast = Disabled

Wireless/Security:
	Security Mode = WPA2 Personal
	Encryption = AES
	Passphrase = [password]
## PC
Desktop:
	IP Configuration = DHCP
Config/Wireless0:
	SSID = [AP_name]
	Authentication:
		WPA2-PSK
		Pass Phrase = [password]
		Encryption Type = AES
	IP Configuration:
		DHCP
___
# Entre Routers
```bash
(config)# interface serial [prot_num]
(config-if)# encapsulation ppp
```
___
# Enrutamiento
- Permite que router llegue a nodos no conectados directamente
CIDR
- Classless ...
- Dinámicos:
	- IGP -> Interior (RIPv2 , EIGRP)
	- EGP -> Exterior

## IRPv2
```bash
(config)# router rip
(config-router)# version 2
//Indico que rutas tengo conectadas directamente
(config-router)# network [ip_classful_red]
(config-router)# no auto-summary
```