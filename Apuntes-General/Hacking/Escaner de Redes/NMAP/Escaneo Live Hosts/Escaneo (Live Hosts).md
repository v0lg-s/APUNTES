La etapa previa al escaneo de puertos consiste en confirmar qué hosts están en línea o *"up"* , se realiza para evitar perder tiempo y generar ruido innecesario en la red escaneando hosts que no existen o no están conectados.

Nmap utiliza 3 diferentes enfoques a la hora de descubrir hosts activos:

1. **[[Descubrimiento usando ARP|ARP Scan:]]** Este tipo de escaneo utiliza "ARP Requests" para descubrir hosts activos en la red.
2. [[Descubrimiento usando ICMP|ICMP Scan:]] Este tipo de escaneo utiliza varios tipos de solicitudes ICMP para identificar hosts activos.
3. [[Descubrimiento usando TCP UDP|TCP/UDP ping scan:]] Este escaneo envía paquetes a puertos TCP/UDP para determinar los hosts activos.

Para esta etapa se debería usar la opción `-sn` **->** realiza un escaneo de ping para determinar qué hosts de la red están en línea, sin escanear activamente los puertos.

**Resumen:**

|  ***Tipo de escaneo***   |            ***Comando de Ejemplo***            |
| :----------------------: | :--------------------------------------------: |
|        *ARP Scan*        |     **`sudo nmap -PR -sn MACHINE_IP/24`**      |
|     *ICMP Echo Scan*     |     **`sudo nmap -PE -sn MACHINE_IP/24`**      |
|  *ICMP Timestamp Scan*   |     **`sudo nmap -PP -sn MACHINE_IP/24`**      |
| *ICMP Address Mask Scan* |     **`sudo nmap -PM -sn MACHINE_IP/24`**      |
|   *TCP SYN Ping Scan*    | **`sudo nmap -PS22,80,443 -sn MACHINE_IP/30`** |
|   *TCP ACK Ping Scan*    | **`sudo nmap -PA22,80,443 -sn MACHINE_IP/30`** |
|     *UDP Ping Scan*      |  `sudo nmap -PU53,161,162 -sn MACHINE_IP/30`   |

| **Opción** |                             **Proposito**                             |
| :--------: | :-------------------------------------------------------------------: |
|    `-n`    |                          No hacer DNS lookup                          |
|    `-R`    | Hacer DNS lookup reverso para todos los hosts (Incluso los inactivos) |
|   `-sn`    |                     Solo descubrir hosts activos.                     |
