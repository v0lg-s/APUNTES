El modelo TCP/IP es un modelo de protocolos porque describe las funciones que ocurren en cada capa de protocolos dentro de una suite de TCP/IP.

![[MODELO-TCP-IP.png]]
![[protocolos por capa TCP IP.png]]
# Capa 4: Aplicación
En esta capa el proceso de encapsulamiento convierte el mensaje en *datos*.

La capa de aplicaciones es el grupo de aplicaciones que requiere comunicación de red. Es con lo que el usuario suele interactuar, como el correo electrónico y la mensajería. Como la capa inferior gestiona los detalles de la comunicación, las aplicaciones no tienen que preocuparse por ello.

Incluye los protocolos utilizados por la mayoría de las aplicaciones para proporcionar servicios de usuario o intercambiar datos de aplicaciones a través de las conexiones de red establecidas por los protocolos de las capas inferiores.
**Protocolos:**
- *HTTP*
- *FTP*
- *SMTP*
- *DHCP*
- *DNS*
- *SSH*
- *TELNET*
# Capa 3: Transporte
Los datos provenientes de la capa superior son encapsulados y se convierten en *segmentos*.

Esta capa admite la comunicación entre distintos dispositivos a través de diversas redes. La capa de transporte tiene 2 tipos de conexiones y son orientada a la conexión como es el TCP, o no orientado a la conexión como es el UDP. Los protocolos de esta capa pueden proporcionar control de errores, segmentación, control de flujo, control de congestión y direccionamiento de aplicaciones.
**Protocolos:**
- *UDP*
- *TCP*
# Capa 2: Internet
Los segmentos que son recibidos de la capa de transporte se encapsulan y se pasan a llamar *paquetes*.
Esta capa se encarga de determinar el mejor camino a través de una red. La capa de Internet es responsable de enviar paquetes de datos a través de múltiples redes. De esta manera, la capa de Internet hace posible la interconexión, el funcionamiento interno de diferentes redes IP y es como Internet se establece.
**Protocolos:**
- *IP*
- *IPv4-IPv6*
- *ARP*

# Capa 1: Acceso al Medio
En esta capa los paquetes de la capa de internet se encapsulan para ser llamados *tramas*.
Controla los dispositivos del hardware y los medios físicos que forman la red. El uso que tiene la capa de enlace es permitir el paso de paquetes entre las interfaces de la capa de Internet de dos hosts diferentes en el mismo enlace.
**Protocolos:**
- *Ethernet*

# Comparación Modelo OSI

El modelo TCP/IP es un método para visualizar las interacciones de los diversos protocolos que conforman el conjunto de protocolos TCP/IP. No describe las funciones generales necesarias para todas las comunicaciones de red. Describe las funciones de red específicas de los protocolos en uso en el conjunto de protocolos TCP/IP.

La funcionalidad de la capa de transporte es la misma en ambos modelos. Sin embargo, la capa de acceso a la red y la capa de aplicaciones del modelo TCP/IP se dividen a su vez en el modelo OSI para describir funciones discretas que deben realizarse en estas capas.

