Usa el [[Protocolo ARP]]
**Plantilla:**
```bash
sudo nmap -PR -sn MACHINE_IP/24
``` 

- *Opción -PR* (**P**ing A**R**P): Utiliza 'ARP Requests' para hacer el escaneo de hosts activos.
- *Opción -sn*: No escanear los puertos de los hosts activos.

Para este tipo de escaneo:

- Se debe estar en la misma LAN, subred o segmento de red que el objetivo. (ARP es un protocolo de capa de enlace, no sale de su red local)
- No es posible usarlo si el host está en otra red.

--- 
**Funcionamiento:**
- El dispositivo que efectúa el escaneo envía un ARP Request (Opcode=2) al/los objetivos, si estos responden con un ARP Reply (Opcode=1) significa que están activos, de lo contario el host está desconectado.

