1. **IP Loopback:** Son direcciones que se usan para que un dispositivo se comunique con sí mismo en una red.
	- **Aplicación:** Se utilizan principalmente para probar y diagnosticar aplicaciones y servicios que utilizan la red.
		- Las direcciones IP de Loopback van en un **rango** de:
			- 127.0.0.0 a 127.0.255.255 → para IPv4
			- : : 1 → Para IPv6
	- **Ejemplo de uso:** Comúnmente se usa la dirección `127.0.0.1` para probar servicios locales en un sistema, como un servidor web o de base de datos, permitiendo conexiones dentro del mismo dispositivo sin acceder a la red externa.

2. **IP APIPA (Automatic Private IP Addressing) o de Enlace Local:** Son direcciones IP reservadas que se utilizan en redes locales cuando un dispositivo no puede obtener una dirección IP válida de un servidor DHCP.

	- **Aplicación:** Las direcciones APIPA son una solución temporal y de último recurso cuando no se puede obtener una dirección IP válida de un servidor DHCP. La falta de conectividad puede indicar problemas en la red o con la configuración de DHCP que deben resolverse para restaurar una conectividad.
		- Están en el **rango** de:
			- 169.254.0.0 - 169.254.255.255
	- **Ejemplo de uso:** Cuando una computadora no recibe una IP por DHCP, puede asignarse una dirección como `169.254.1.1`, permitiendo la comunicación con otros dispositivos en la misma red que también tienen direcciones de enlace local.
	
3. **Direcciones de Test-Net**

	- **Rango:** `192.0.2.0 - 192.0.2.255`
	- **Aplicación:** Estas direcciones están reservadas para ser utilizadas en ejemplos y documentación, y nunca deben ser utilizadas en redes reales. Se utilizan cuando se describen redes o se explican conceptos, pero no se espera que se conecten a sistemas reales.
	- **Ejemplo de uso:** En la documentación, es común ver ejemplos con direcciones como `192.0.2.1` para mostrar cómo configurar una red sin interferir con las direcciones reales de una red operativa.