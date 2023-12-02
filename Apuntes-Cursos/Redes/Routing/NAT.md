# NAT - (Network Address Translation)
## ¿Qué es NAT?
Es una técnica que surgió para suplir el agotamiento de direcciones IPv4.
Entre las otras técnicas se encuentran:
→ Bloque de Direcciones Privadas.
→ Direccionamiento sin clases (CIDR).

## Utilización de NAT
Dado que solo las direcciones IP públicas son enrutables en internet (significa que los enrutadores y servidores en Internet pueden enviar paquetes de datos a esa dirección IP, y esos paquetes de datos llegarán a su destino correspondiente.) Si queremos que nuestros dispositivos con IP privadas se conecten a internet tendremos que usar *NAT*.

**NAT** se encarga de tomar direcciones IP privadas de una LAN y mapearlas o traducirlas en una IP pública enrutable.

### Fundamento
Si podemos conectarnos a internet con direcciones IP públicas ¿por qué no solo usar estas direcciones?

El fundamento del uso de NAT se basa en:
1. Arrendar varias IP's públicas es costoso.
2. No hay tantas IPv4 públicas como para que cada dispositivo final use una.
3. Se pueden conectar miles de nodos a internet haciendo uso de una sola IP pública.


## Tipos de NAT

**Funcionamiento**
NAT en una red local se comporta de la siguiente manera, 
1. El router recibe una trama de datos con una dirección IP origen privada de algún dispositivo de su red. 
2. El router mediante NAT traduce esta dirección IP en una IP pública (única en toda la red).
3. El router guarda la información del puerto y la IP privada del tráfico saliente en una tabla para que cuando reciba paquetes dirigidos a ese dispositivo los pueda redirigir sin problema.
---
1. *NAT Estática (SNAT):* Una dirección privada es siempre traducida a una misma dirección pública. 
	- Este tipo de NAT es usado en redes de servidores, por ejemplo, en este tipo de redes no existe un tráfico saliente como en una red doméstica de dispositivos finales, todo el tráfico es entrante. Es por esto que el router asigna una dirección IP pública particular a un dispositivo (servidor) dentro de su red para que cuando llegue un paquete para el dispositivo llegue directamente a este. (No debe ser usada en redes domésticas porque representa un riesgo de seguridad al mostrar nuestro dispositivo a internet directamente.)
2. *NAT Dinámica (DNAT):* El router tiene un grupo de direcciones IP públicas asignadas a dispositivos con direcciones IP privadas por lo que cada una tiene por lo menos una IP pública asignada.
3. *NAT con Sobrecarga o PAT (Port Address Translation):*  Todos los dispositivos con direcciones IP privadas en una red comparten una única dirección IP pública al salir de la red. Para lograr esto el router hace lo siguiente: ^7db95a
	- El router hace uso de los 65.536 puertos definidos en los protocolos TCP y UDP para realizar conexiones.
	- Cuando un dispositivo quiere establecer una conexión fuera de su red, el router almacena su IP privada y su puerto de origen y los relaciona con una IP pública y un puerto al azar.
		![[PAT 1.png|500]]
	- Cuando llega información a esa IP pública y a ese puerto elegido al azar, el router reenvía esa información a la IP privada y al puerto de origen inicial que se encuentran relacionados en la tabla.  
		![[PAT 2.png|500]]

4. *NAT de Solapamiento:* Se usa cuando las direcciones IP privadas de una red coinciden con las direcciones IP públicas en uso de otra red, el NAT transforma estas direcciones en IP's públicas únicas.
