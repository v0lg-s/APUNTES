El modelo OSI (Open Systems Interconnection) es un modelo que permite mostrar visualmente lo que puede acontecer en el intercambio de datos entre 2 sistemas en red. Lo hace ordenando por capas o niveles los distintos procesos de comunicación que se llevan a cabo a la hora de trasladar datos de un sistema a otro conectado también en una red.

Antes de que se envíe cualquier información por un dispositivo en la red, debe pasar por distintos procesos en cada capa del modelo OSI.

Cada capa tiene sus [[Qué es un Protocolo|protocolos]] específicos.
![[modelo-OSI.jpg|550]]
# Capa 1: Capa Física 
Se asegura de que los datos en 1's y 0's se muevan entre distintos hosts. Describe los medios físicos para mantener y desactivar las comunicaciones.
- **Tiene especificaciones cómo:**
	- Grosor de un cable que se usa para el cableado de una red.
	- Frecuencia de radio que se usará en la comunicación.
	- Integridad de las conexiones.
	- Estándares físicos acerca de la red.

# Capa 2: Enlace de Datos
Describe los métodos para intercambiar tramas de datos entre dispositivos en un medio común LAN.
- **Esta capa se encarga de:**
	- Verificar la integridad de los datos.
	- Verificar la dirección MAC en una trama de datos para saber a que dispositivo va dirigida esa trama.
	- Dentro de esta capa están los dispositivos intermediarios como los switches.
	- Hace que se produzca la transferencia de datos.
- La capa 2 usa las direcciones MAC de los dispositivos.
- Esta capa se asegura que las tramas de datos lleguen al lugar correcto.
## Subcapas
1. **LLC (Control de Enlace Lógico):** Convierte las señales físicas recibidas ya sea, por medio de electricidad, luz o radiofrecuencia, en 1's y 0's.
2. **MAC (Control de Acceso al Medio)**: Mueve los paquetes de datos desde la interfaz de red o NIC hasta otra interfaz.


Después que la capa 2 se encarga de direccionar y verificar la integridad de los datos mediante la dirección MAC, envía el resto de la trama de datos hacia la siguiente capa.

# Capa 3: Capa de Red
Proporciona servicios para intercambiar los datos individuales en la red entre terminales identificados.
- Esta capa tiene procesos como el enrutamiento llevado a cabo por routers o switches de capa 3.
- Opera con las direcciones IP.
- Figurativamente esta capa se puede ver como un agente de tránsito de la red. Dirige las tramas de datos a sus destinos.
Se debe trabajar con direcciones IP ya que al conectarse a internet las direcciones MAC son insuficientes.
## Protocolos Capa de Red
- **OSPF**: Protocolo que determina la ruta más rápida que deben seguir los datos para llegar a su destino dentro de una red.
- ==IP== 
- IPsec
- [[Protocolo ARP|ARP]]
- [[NAT|NAT]]
- ICMP

# Capa 4: Capa de Transporte

^ebf795
Define los servicios para segmentar, transferir y ensamblar los datos para las comunicaciones individuales.
- **Esta capa se encarga de:** 
	- *Desensamblar y Reensamblar datos:* Una trama ethernet o de datos solo puede contener 1500 bytes como máximo. Si se requiere enviar un archivo más grande se debe desensamblar en tramas de 1500 bytes y posteriormente reensamblar todo el mensaje. Si los datos vienen entrando a la capa, esta misma las desensambla.
	- *Coordinar todo el tránsito de datos*
		- ==*Velocidad con la que se materializará la comunicación.*==
		- ==*Cuál es el destino.*==
		- ==*Qué puertos se usarán.*==
- **Posibles incidencias:**
	- Que los datos  no se puedan enviar porque los puertos que se van a emplear están cerrados.

## Protocolos Capa de Transporte
Protocolos de transmisión de datos.
- [[Protocolo TCP#TCP (Transmission Control Protocol)|TCP]]
- [[Protocolo TCP#UDP (User Datagram Protocol)|UDP]]

# Capa 5: Capa de Sesión
Es la parte del [[Roles de Cliente y Servidor#^6e841b|Host]] transmisor que ==hace la conexión== con el host remoto o receptor. Aquí se hace la conexión a los diferentes servicios dependiendo de la solicitud del cliente.
- **Ejemplo:** 
	- Conexión a un servidor web desde un navegador web.
	- Conexión a un servidor de correo electrónico si se trata de un cliente email.
## Funcionalidad
- El número de puerto definido en la [[#^ebf795|capa anterior]] y que se incluye en la trama de datos es el que envía la información a la aplicación correcta.
- Esta capa toma el número de puerto de destino y envía los datos a la aplicación que es alojada por el puerto especificado.

# Capa 6: Capa de Presentación
Antes de pasar a la aplicación los datos deben pasar por la presentación que se encarga de darle un formato presentables los datos de tal manera que la aplicación los pueda interpretar.
- Puede incluir la desencriptación o conversión de los datos.

# Capa 7: Capa de Aplicación
Se encarga de la comunicación entre la app y la red, pueden ser aplicaciones como navegadores web.

## Protocolos de la Capa de Aplicación
- HTTPS
- DNS
- FTP
- SMTP