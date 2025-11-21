```bash

```
# CLI
Seguridad: 
```bash
//contraseña para enable
(config)# enable secret [enable_password]

//contraseña para config
(config)# line console 0 
(config-line)# password [password]
(config-line)# login

//contraseña para acceso remoto (telent/ssh)
(config)# line vty [rango_de_puertos]
(config-line)# password [password]
(config-line)# login
```
Modos:
```bash
[Switch_name]> enable
[Switch_name]# config
[Switch_name](config)# line vty [puerto_inicio] [pruerto_final]
[Switch_name](config-line)# 

// rango de interfaces -> 0/[inicio]-[fin]
[Switch_name](config)# interface f 0/[nro_interfaz]
[Switch_name](config-if)#
```

Acceso Remoto:
```bash
//Telnel
(config-line)# password [password]
(config-line)# exec-timeout [time_out_minutes]
(config-line)# transport input telnet

//Ssh
	//configurar dominio, usar rsa de 768
(config)# ip domain-name [nombre_dominio]
(config)# crypto key generate rsa 
	//configurar ssh
(config)# ip ssh version 2

(config-line)# transport input ssh
(config-line)# exec-timeout [time_out_minutes]
(config-line)# login local
(config-line)# password [password]
(config-line)# username [username] privilege [nro_privilege] password [password]
```

Interfaces:
```bash
//Deshabilitar interfaz
(config-if)# shutdown

(config-if)# switchport mode access 
(config-if)# switchport port-security
(config-if)# switchport port-security maximum 1
(config-if)# switchport port-security mac-address [mac_addr]
(config-if)# switchport port-security violation shutdown
```

Vlan:
```bash
(config)# vlan [nro_new_vlan]
(config)# name [name_vlan]
---------------------------------------
//Configurar puerto al que está conectada la PC
(config-if)# switchport access vlan [nro_vlan]
---------------------------------------
//Configurar el puerto para que permita pasar conexiones de vlans (entre 2 switches)
(config-if)# switchport mode trunk
```

Load Balancer:
```bash
(config)# spanning-tree vlan [nro_vlan],[nro_vlan], ... root primary

//dst-mac => Balancea por mac destino ; src-mac => Balancea por mac origen
(config)# prot-channel load-balancer {dst-mac;src-mac}
(config)# interface gigabitethernet [nro_interface]
(config-if)# switchport mode trunk
(config-if)# channel-protocol LACP
(config-if)# channel-group 1 mode active 
```