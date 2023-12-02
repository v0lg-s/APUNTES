DHCP (Dynamic Host Configuration Protocol) es un protocolo que trabaja en la [[Modelo OSI#Capa 7 Capa de Aplicación|Capa de Aplicación]], su función principal es asignar direcciones IP de manera dinámica a dispositivos dentro de una red, además, hace automáticamente la configuración TCP/IP (Configuraciones como la Máscara de Red, Dirección IP, servidor DNS, router por defecto o Default Gateway). Esta configuración es necesaria para cada dispositivo que se conecta a la red.

Bootstrap Protocol es el protocolo homólogo de DHCP en sistemas Linux.

Solo puede haber un servidor DHCP en la red, si hay más de uno puede crear conflictos. El servidor debe estar dentro de la red.

DHCP es generalmente el método preferido para asignar direcciones IP a los hosts de grandes redes, dado que reduce la carga para al personal de soporte de la red y prácticamente elimina los errores de entrada. Sin embargo, el propio DHCP no discrimina entre dispositivos autorizados y no autorizados y asignará parámetros de configuración a todos los dispositivos solicitantes. Los servidores DHCP generalmente están configurados para asignar direcciones de un rango de subred, por lo que no hay garantía de que cada dispositivo que necesita una dirección obtenga una.
# Funcionamiento
El funcionamiento básico del DHCP implica los siguientes componentes:

1. **Cliente DHCP:** Cada dispositivo que se conecta a una red y necesita una dirección IP, como una computadora, teléfono o impresora, actúa como cliente DHCP.
    
2. **Servidor DHCP:** En la red, existe al menos un servidor DHCP que administra y distribuye direcciones IP y configuraciones de red. Este servidor puede ser un enrutador, un servidor dedicado o una función incorporada en otro dispositivo de red. Puede responder peticiones desde muchas subredes.

**Proceso de Asignación:**

1. Cuando un dispositivo se conecta a la red, el *cliente DHCP* envía un mensaje llamado "DHCP Discover" a través de la red local con dirección Broadcast en busca de un servidor DHCP disponible.
2. El *servidor DHCP* recibe la solicitud y, si tiene direcciones IP disponibles, selecciona una de ellas y la asigna al cliente. También proporciona otros detalles de configuración, como la máscara de subred, la puerta de enlace y la dirección del servidor DNS. El servidor envía toda esta información a través de un mensaje llamado "DHCP Offer" con dirección Unicast al cliente DHCP.
3. El *cliente DHCP* acepta la dirección IP asignada y aplica la configuración proporcionada por el servidor. Y envía un mensaje "DHCP Request" comunicándole al servidor que acepta su oferta.
4. El *servidor DHCP* responde con un mensaje "DHCP Acknowledgement" comunicando que confirma la recepción de aceptación y que pondrá en funcionamiento toda la configuración dada.