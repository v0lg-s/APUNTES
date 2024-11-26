¿Cómo se asegura la tarjeta de red que los datos lleguen a la aplicación correcta dentro de la PC?
¿Cómo se asegura que la información llegue al computador de destino completa y utilizable?

Los puertos son utilizados para redirigir la información que llega en las tramas de datos a la aplicación correcta. Los números de puertos son agregados a la trama de ethernet (puerto de destino y origen).

- **Puertos Bien Conocidos**: Van desde el número 0 hasta el 1.023. Estos puertos están asignados a servicios específicos y se reservan para aplicaciones comunes. Por ejemplo, el puerto 80 se usa para HTTP (navegación web), el puerto 25 para SMTP (correo electrónico saliente) y el puerto 53 para DNS.
    
- **Puertos Registrados:** Van desde el número 1.024 hasta 49.151. Estos puertos son registrados por algunas aplicaciones para evitar conflictos. 

- **Puertos Dinámicos:** Van desde el 49.152 hasta el 65.535. Son puertos disponibles para ser usados por el sistema o por algunas aplicaciones si es necesario.

![[puertos-PROTOCOLOS.png]]

## Puertos conocidos con aplicaciones asociadas:

| Número de Puerto | Transporte |                   Protocolo de aplicación                    |
| :--------------: | :--------: | :----------------------------------------------------------: |
|        20        |    TCP     |                         FTP - Datos                          |
|        21        |    TCP     |                        FTP - Control                         |
|        22        |    TCP     |                       Secure Shell SSH                       |
|        23        |    TCP     |                            Telnet                            |
|        25        |  UDP, TCP  |      Protocolo simple de transferencia de correo (SMTP)      |
|       587        |  UDP, TCP  |  Protocolo simple de transferencia de correo seguro (SMTPS)  |
|        53        |  UDP, TCP  |             Servicio de nombres de dominio (DNS)             |
|        67        |    UDP     |                       DHCP - Servidor                        |
|        68        |    UDP     |                        DHCP -Cliente                         |
|        69        |    UDP     |    Protocolo trivial de transferencia de archivos (TFTP)     |
|        80        |    TCP     |                             HTTP                             |
|       110        |  UDP, TCP  | Protocolo de oficina de correos, versión 3 (POP3) No cifrado |
|       995        |  UDP, TCP  | Protocolo de oficina de correos, versión 3 (POP3) Encriptado |
|       143        |    TCP     | Protocolo de acceso a mensajes de Internet (IMAP) No cifrado |
|       993        |    TCP     | Protocolo de acceso a mensajes de Internet (IMAP) Encriptado |
|       161        |    UDP     |      Protocolo simple de administración de redes (SNMP)      |
|       443        |    TCP     |   Protocolo seguro de transferencia de hipertexto (HTTPS)    |

Se puede ver el sitio web de IANA para consultar el registro de puertos con la lista completa de números de puerto y la aplicación asociada.

