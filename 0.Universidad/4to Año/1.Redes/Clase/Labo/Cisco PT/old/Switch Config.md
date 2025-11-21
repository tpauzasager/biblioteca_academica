 Entrar a CLI del switch
	- Directo por PT (en CLI del switch)
	- Agregando laptop, conectando con cable (azul) y por CLI de laptop 

Entrar a sudo
	- enable

Entrar a modo configuración
	- configure

Persistir cambios de configuración 
	- copy runing-config startup-config

# Crear Vlan
1. en switch
	(config)# vlan <número de vlan>
	(config-vlan)# name <nombre vlan/> 
2. Agregar los cables directos de pc a switch
3. En switch (asignar vlan a un puerto)
	(config)# interface <numero de puerto/> (ej f0/1)
	(config-if)# switchport access vlan <num vlan/>
	(config-if)# switchport mode access 
4. Si tengo vlans entre varios switchs, conectar este switch a los demás y configurar dicho puerto como track (en ambos switch)
	- Cable cruzado entre switches y ejecutar en el puerto del cable
	(config-if)# switchport mode trunk     <- en cada switch
	(config-if)# switchport trunk allowed vlan <lista de num de vlans/> (separados por ,)    <- opcional

# TelNet
1. Conectar cable directo desde pc hasta switch (opcional?)
2. En switch
	1. (config)# line vty <nro_inicio/> <nro_fin/>      (indico rango de puertos dedicados para conexión en paralelo, ej 0 1)
	2. (config-line)# password <password para la conexión/>
	3. (config-line)# exec-timeout <numero/>
	4. (config-line)# transport input telnet 
# Ssh
1. Configurar dominio 
	(config)# ip domain-name <nombre dominio/>
	(config)# crypto key generate rsa 
2. configurar vty
	(config)# line vty <inicio/> <fin/>
	(config-line)# transport input ssh 	
	(config-line)# login local        <- guardar user/pass localmente
	(config-line)# exec-timeout 5
	(config-line)# username <nombre/> privilege <nro_privilegio/> secret <password/>
3. En PC conectarse por ssh
	ssh -l <user_name/> <server_ip/> 
	<password/> 