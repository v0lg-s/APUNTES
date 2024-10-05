# Dirección IP Pública Vs Privada

**IP Pública:** es la que identifica nuestra red desde el exterior., es asignada por el proveedor de internet y puede ser dinámica o estática. Ejemplo:
- Es la dirección del conjunto residencial, esta dirección permite ubicarlo desde cualquier punto de la ciudad.

**IP Privada:** es la que identifica a un dispositivo conectado en nuestra red interna., es asignada por el router, es dinámica y modificable.
-  Direcciones que empiezan con:
	- 10.x.x.x 
	- 172.16.x.x - 172.31.x.x
	- 192.168.x.x 

**IP Loopback:** Son direcciones que se usan para que un dispositivo se comunique con sí mismo en una red.
- Se utilizan principalmente para probar y diagnosticar aplicaciones y servicios que utilizan la red.
	- Las direcciones IP de Loopback son:
		- 127.0.0.1 o 127.0.x.x → para IPv4
		- : : 1 → Para IPv6

**IP APIPA (Automatic Private IP Addressing):** Son direcciones IP reservadas que se utilizan en redes locales cuando un dispositivo no puede obtener una dirección IP válida de un servidor DHCP.

Las direcciones APIPA son una solución temporal y de último recurso cuando no se puede obtener una dirección IP válida de un servidor DHCP. La falta de conectividad puede indicar problemas en la red o con la configuración de DHCP que deben resolverse para restaurar una conectividad.
- Están en el rango de:
	- 169.254.0.0 - 169.254.255.255