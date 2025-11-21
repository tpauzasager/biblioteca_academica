# Dirección IP
- Para internet 
- Tamaño = 32b 
- **Identifica el puerto** de comunicación (no al dispositivo)

Componentes 
	- Identificador de clase (solo si es con clase - para identificar formato de la dir)
	- Número de red (único)
	- Número de host (único dentro de cada red)
Dir Especiales:

| Nombre                     | Red     | Port/Host | Uso                                                                                    |
| -------------------------- | ------- | --------- | -------------------------------------------------------------------------------------- |
| Difusión Dirigida          | A       | 255.255   | Envia a todos los puertos de la red A                                                  |
| Difusión Limitada          | 255.255 | 255.255   | Envía a todos los puertos de la LAN en la que está el disp                             |
| Identificador<br>de Red    | A       | 000.000   | Es el identificador de la red A (no se envía en datagrama)                             |
| Identificación <br>de Host | 000.000 | 000.000   | Para arranque (datagrama no va a ningun lado)                                          |
| Loopback                   |         |           | [127.0.0.0; 127.25.255.255] (solo se usa 127.0.0.1) <br>Se usa para autorreferenciarse |
