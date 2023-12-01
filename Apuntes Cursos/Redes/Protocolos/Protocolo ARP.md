---

---
---
Es un protocolo usado en la [[Modelo OSI#Capa 2 Enlace de Datos | capa 2 de enlace de datos ]], este protocolo es usado para identificar la dirección MAC de un dispositivo teniendo antes su dirección IP, todo esto para enviar datos dentro de una red ethernet o local.

- Significa Protocolo de Resolución de Direcciones por sus siglas en inglés (Address Resolution Protocol) 
- El protocolo *nd o detección de vecinos* es el protocolo equivalente pero que usa direcciones IPv6.

# Funcionamiento

1) Si un computador se quiere comunicar con otro en la misma red realiza el proceso de encapsulamiento desde la capa 7 hasta la 2, por lo que, cuando la trama viene de la [[Modelo OSI#Capa 3 Capa de Red | capa de red]] ya viene con una dirección IP de destino encapsulada, por lo que la información necesaria de esta capa ya está completa, sin embargo, en la capa 2 la trama solo tiene la dirección MAC de origen pero desconoce la dirección de destino. 
2) Por lo tanto, el computador o maquina remitente creará una trama ARP (se habla de tramas por ser capa 2) con dirección de destino [[Broadcast y Unicast#Broadcast | broadcast]] para que todos los dispositivos en la red local tengan una copia de esta trama.
3) La trama ARP contiene figurativamente una pregunta: "¿Quien tiene la dirección IP: 30.0.0.53?"
4) Todos los equipos reciben la trama pero como una dirección IP distinta a la suya se encuentra en la cabecera de la trama la descartarán.
5) Cuando el dispositivo con la dirección IP 30.0.0.53 reciba la trama, responderá de manera [[Broadcast y Unicast#Unicast | unicast]] con la dirección del computador que envió la trama ARP. Su respuesta contendrá la respuesta a la pregunta hecha por la trama ARP. "Yo tengo esa dirección IP, mi MAC es la siguiente: 40-8D-5C-1C-5A-50".
6) El computador remitente relaciona en su tabla ARP la dirección IP del computador receptor 30.0.0.53 con la dirección MAC 40-8D-5C-1C-5A-50, para que se puedan enviar las tramas a dicho computador sin necesidad de hacer este proceso nuevamente.

Se puede usar el comando *arp -a* para mostrar la tabla ARP.
![[arp -a.png]]
# Trama ARP
![[trama-ethernet.png]]
## Fase de Petición

En esta fase la maquina que desea conocer la dirección MAC de otra crea la trama ARP y la envía preguntando por esta.

- **Destino y Origen:** La trama enviada durante la fase de petición contiene en el campo de origen la dirección MAC del computador remitente y en el campo de destino se encuentra la dirección [[Broadcast y Unicast#Broadcast |broadcast]].
- **Tipo/Longitud:** La trama ARP tendrá en este campo el valor *0x0806* que indica que se trata de una trama del tipo ARP. (*0x-* indica que el valor después de la x está en notación hexadecimal)
- **Datos:** El encabezado ARP se encuentra en el espacio de los datos.

## Fase de Respuesta

En esta fase la maquina de la que se desconoce su dirección MAC envía una trama ARP con la respuesta.

- **Destino y Origen:** La trama enviada durante la fase de respuesta contiene en el campo de origen la dirección MAC del computador que recibió la trama ARP en la fase de petición y en el campo de destino se encuentra la dirección MAC del computador que envió la trama ARP

# Encabezado ARP
![[encabezado-ARP.png]]

- **Hardware Type:** Indica el protocolo de capa 2. En este caso es Ethernet con código (1).
- **Protocol Type:** Indica el protocolo de capa 3. En este caso IPv4 con código (0x0800). 
	- Estos dos campos son usados para que ARP sepa que tipo de direcciones se van a usar.
- **Hardware Address Lenght:** Se define el ==tamaño== de la ==dirección MAC==. En este caso 6 bytes.
- **Protocol Address Lenght:** Se define el ==tamaño== de la ==dirección IP==. En este caso 4 bytes.
- **Operation Code (OpCode):** Toma 2 valores dependiendo de la fase del protocolo ARP. 
	- 1: Si es la fase de petición.
	- 2: Si es la fase de respuesta.

Para el ejemplo, PC_1 se desea comunicar con PC_2 y necesita conocer su dirección MAC.

- **Sender Hardware Address:** Dirección MAC del remitente.
	- *Fase de Petición:* Dirección MAC de PC_1.
	- *Fase de respuesta:* Dirección MAC de PC_2. (Lo que se desea conocer)
---- 
- **Sender Protocol Address:** Dirección IP del remitente.
	- *Fase de Petición:* Dirección IP de PC_1.
	- *Fase de respuesta:* Dirección IP de PC_2.
---
- **Target Hardware Address:** Dirección MAC del receptor. 
	- *Fase de Petición:* Todo 0's. (Se desconoce)
	- *Fase de respuesta:* Dirección MAC de PC_1.
-------
- **Target Protocol Address:** Dirección IP del receptor.
	- *Fase de Petición:* Dirección IP de PC_2.
	- *Fase de respuesta:* Dirección IP de PC_1.

