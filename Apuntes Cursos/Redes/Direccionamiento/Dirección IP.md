Ya que las direcciones MAC no identifican que un grupo de computadores pertenecen a una [[Tipos de Redes#^4b7544|red local]] específica se hacen necesarias las direcciones IP para identificar redes y dispositivos al tiempo.

Como lo dice su nombre una dirección IP es literalmente una dirección (número) que identifica un dispositivo en internet. Así como una casa en una ciudad tiene una dirección para saber cómo llegar, un dispositivo en internet tiene su dirección IP única.

- Son usadas para el enrutamiento y segmentación:
	- **Enrutamiento de datos:** En redes de mayor escala, como Internet, los datos deben ser enviados a través de múltiples nodos intermedios antes de llegar a su destino final. Las direcciones IP permiten que los routers y otros dispositivos de red identifiquen el camino correcto para enrutar los datos hacia su destino.
	- **Segmentación de redes:** Las redes grandes pueden dividirse en segmentos más pequeños para facilitar la administración y mejorar el rendimiento. Cada segmento puede tener su propio rango de direcciones IP, lo que ayuda a mantener el orden y la organización en la red. (Ver [[Subnetting | subnetting]])
- Es un requisito para conectarse a internet para que otros dispositivos puedan enviar y recibir datos de el dispositivo.

# Características
- No están fijadas a una tarjeta de red específica.
- Son únicas.
- Se puede usar para identificar una red en particular.
- Pueden cambiar.
- Son números entre 0-255.
Una dirección IP luce así después de ser convertida al sistema decimal:  

		192.168.1.1

Son escritas como 4 octetos binarios.

		11000000.10101000.00000001.00000001

 Los primeros tres números, es decir, ==192.168.1== identifican a la red. El último número identifica al dispositivo conectado a esa red. Lo anterior teniendo en cuenta la [[Máscaras de Subred | máscara de red]].
*Nota:* En realidad el computador no tiene los puntos que dividen los octetos, son notaciones para facilitar la lectura.
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
# Dirección IP Estática Vs Dinámica

**Dirección IP Estática:**

1. **Características:**
    - Una dirección IP estática es una dirección IP que se asigna permanentemente a un dispositivo en una red.
    - No cambia con el tiempo, a menos que se realice una reconfiguración manual.
    - Suele asignarse manualmente por un administrador de red o configurarse en el propio dispositivo.
    - Es constante y predecible.
2. **Casos de Uso:**
    - Se utiliza en servidores y dispositivos de red que deben estar siempre disponibles en la misma dirección, como servidores web, servidores de correo, cámaras de seguridad, etc.
    - Es útil para servicios que necesitan ser accesibles de manera consistente a través de la misma dirección IP, como aplicaciones remotas o VPN.
    - Se emplea en situaciones donde es importante tener un control total sobre la asignación de direcciones IP.

**Dirección IP Dinámica:**

1. **Características:**
    - Una dirección IP dinámica es una dirección IP que se asigna automáticamente a un dispositivo por un servidor [[Protocolo DHCP|DHCP (Protocolo de Configuración Dinámica de Host)]] en la red.
    - Puede cambiar con el tiempo cuando un dispositivo se conecta o desconecta de la red, pero la asignación es temporal y se libera cuando el dispositivo no está en uso.
    - Es eficiente en la gestión de direcciones IP, ya que permite compartir un grupo limitado de direcciones IP entre varios dispositivos en función de su disponibilidad.
2. **Casos de Uso:**
    - Es ampliamente utilizado en redes domésticas y entornos empresariales para dispositivos cotidianos como computadoras, teléfonos, tabletas y otros dispositivos móviles.
    - Es eficiente en la asignación de direcciones IP en redes con muchos dispositivos, ya que permite que los dispositivos compartan direcciones IP de manera dinámica sin requerir una dirección IP única para cada uno.
    - Facilita la administración de la red al eliminar la necesidad de configurar manualmente cada dispositivo con una dirección IP específica.