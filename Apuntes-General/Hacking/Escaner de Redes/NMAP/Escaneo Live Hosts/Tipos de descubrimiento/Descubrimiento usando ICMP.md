Usa el [[Protocolo ICMP]]

En muchas redes se restringe el reenvío de cierto tipo de paquetes por razones de seguridad, para evadir esto:
- Se debe tener en cuenta que existen multiples tipos de paquetes ICMP, Nmap contempla esto y existen distintas opciones para elegir que tipo de paquete enviar. 
	- Tipo 8 (*Echo*) y Tipo 0 (*Echo reply*): Se usan cuando se hace ping.
	- Tipo 13 (*timestamp request*) y Tipo 14 (*timestamp reply*)
	- Tipo 17 (*address mask queries*) y Tipo 18 (*address mask replies*)
**Plantilla:**
```bash
sudo nmap -PE -sn MACHINE_IP/24
sudo nmap -PP -sn MACHINE_IP/24
sudo nmap -PM -sn MACHINE_IP/24
``` 

- *Opción -PE (Ping Echo):* Utiliza *tipo 8* y *tipo 0* para hacer el escaneo de hosts activos.
- *Opción -PP:* Utiliza *tipo 13* y *tipo 14* para hacer el escaneo de hosts activos.
- *Opción -PM (Ping Mask):* Utiliza *tipo 17* y *tipo 18* para hacer el escaneo de hosts activos.
- *Opción -sn*: No escanear los puertos de los hosts activos.

Para este tipo de escaneo:

1.  Se utiliza cuando el objetivo está fuera de la red local del dispositivo que ejecuta el escaneo.

---
**Funcionamiento**
- **-PE:** Hace ping a los objetivos. Envía *Echo Request* y espera un *Echo Reply*, si lo recibe de x host es señal de que el host x está activo.
- **-PP:** Envía *Timestamp Request* y espera un *Timestamp Reply*, si lo recibe de x host es señal de que el host x está activo.
- **-PM:** Envía *Address mask request* y espera un *Address mask reply*, si lo recibe de x host es señal de que el host x está activo.

