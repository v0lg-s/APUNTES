3 Categorías:
## Protocolos de comunicación
Rigen el intercambio de información en una transmisión por red. **Cómo se transmiten los datos entre dispositivos. Métodos para recuperar datos perdidos en tránsito.**

### Protocolos ya documentados por mí (Revisarlos)
- [[Protocolo TCP]]: Protocolo de comunicaciones de internet, permite que dos dispositivos formen una conexión y se lleve a cabo una transmisión de información.
- [[Protocolo ARP]]: Usado para determinar la dirección MAC del siguiente router o dispositivo en el camino.
- [[Protocolo UDP]]: Es un protocolo no orientado a la conexión, es decir, comienza la transmisión sin antes establecer una conexión entre ambos dispositivos. Se usa para transmisiones cuyo requerimiento sea la velocidad. 
	- **Ejemplo:** Se usa UDP para enviar solicitudes DNS a servidores DNS locales.

### Protocolos nuevos dados en el curso (Profundizar)
#profundizar

- **Protocolo de Transferencia de Hipertexto HTTP:** Protocolo de la capa de aplicación, proporciona un método de comunicación para enviar y recibir sitios web. Funciona por el puerto 80. Se considera inseguro porque no cifra los datos intercambiados. Su versión segura es HTTPS que utiliza encriptación SSL/TLS para la comunicación.
- **Sistema de Nombres de dominio DNS:** Este protocolo traduce los nombres de dominio de internet (por ejemplo, facebook.com, wikipedia.org, google.com) en direcciones IP del servidor que aloja esos dominios. Usa el puerto 53 junto a UDP. Si la respuesta del servidor DNS es muy grande, utilizará TCP. (Capa de aplicación)

## Protocolos de Gestión
Se utilizan para supervisar y gestionar la actividad en una red. **Notifican errores y optimizan el rendimiento en la red.**

### Protocolo ya documentado por mí (Profundizar)
#profundizar 
- [[Protocolo ICMP]]: Utilizado por dispositivos para informarse mutuamente de los errores de transmisión de datos a través de la red. El dispositivo receptor envía un informe al dispositivo emisor sobre la transmisión de datos. ICMP es el protocolo usado por el comando `"ping"` (Capa de internet)

### Protocolo nuevo dado en el curso (Profundizar)
#profundizar 
- **Protocolo Simple de Administración de Red SNMP:** Supervisa y gestiona los dispositivos de una red. Puede restablecer una contraseña en un dispositivo de red o cambiar su configuración base. Puede enviar solicitudes a los dispositivos de red para obtener un informe sobre la cantidad de ancho de banda de la red que se está utilizando. (Capa de Aplicación)

## Protocolo de Seguridad
Garantizan que los datos se envían y reciben de forma segura a través de una red. Usan algoritmos de encriptación para proteger los datos en tránsito.

- **HTTPS**: Lo mismo que HTTP pero usa encriptación secure sockets layer/transport layer security en todas las transmisiones. Usa el puerto 443. (Capa de aplicación)
- **Protocolo Seguro de Transferencia de Archivos SFTP:** Protocolo seguro para transferir archivos de un dispositivo a otro a través de una red. SFTP usa Secure Shell(SSH) a través del puerto TCP 22. SSH usa el estandar de encriptación avanzada (AES). Se utiliza a menudo con el almacenamiento en la nube. Al subir o bajar un archivo de la nube se usa SFTP. (Capa de aplicación).

## Adicionales
- [[NAT]]
- [[Protocolo DHCP]]
- [[Protocolo SSH]]
- **Telnet:** Es un protocolo usado para conectarse a un sistema de manera remota. No cifra la información, la envía en texto claro. Usa el puerto TCP 23. La alternativa segura de este protocolo es SSH. (Capa de Aplicación)
- **Protocolo de Oficina de Correos POP (Post Office Protocol):** Gestiona y recupera correo electrónico de un servidor de correo. POP3 es la versión más utilizada. Muchas organizaciones tienen un servidor de correo dedicado en la red que gestiona el correo entrante y saliente para los usuarios de la red.
	- Los dispositivos de los usuarios enviarán solicitudes al servidor de correo remoto y descargarán los mensajes de correo electrónico localmente.
	- La autenticación en texto plano sin cifrar utiliza el puerto TCP/UDP 110 y los correos electrónicos cifrados utilizan la Capa de sockets seguros/Seguridad de la capa de transporte (SSL/TLS) a través del puerto TCP/UDP 995.
	- El correo puede o no permanecer en el servidor. 
- **Protocolo de Acceso a Mensajes de Internet (IMAP):** Se utiliza para el correo electrónico entrante. Descarga las cebeceras de los correos electrónicos y el contenido del mensaje.
	- IMAP utiliza el puerto TCP 143 para el correo electrónico no cifrado y el puerto TCP 993 a través del protocolo TLS.
	- El contenido también permanece en el servidor de correo electrónico, lo que permite a los usuarios acceder a su correo electrónico desde múltiples dispositivos.
- **Protocolo Simple de Transmisión de Correo (SMTP):** Transmite y encamina el correo electrónico del remitente a la dirección del destinatario. Funciona con el software de Agente de Transferencias de Mensajes (MTA), que busca en los servidores DNS para resolver las direcciones de correo electrónico en direcciones IP.
	- SMTP utiliza el puerto TCP/UDP 25 para los correos electrónicos no cifrados y el puerto TCP/UDP 587 que utiliza TLS para los correos electrónicos cifrados.
	- El puerto TCP 25 suele ser utilizado por el spam de gran volumen. SMTP ayuda a filtrar el spam regulando cuántos correos electrónicos puede enviar una fuente a la vez.

![[Puertos#Puertos conocidos con aplicaciones asociadas]]