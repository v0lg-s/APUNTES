![[formatoPaqueteIPv4.png]]
- **Tamaño del encabezado:** El tamaño varía entre 20 y 60 bytes.
	- Los primeros 20 bytes son un conjunto de información con datos como la IP de destino y origen, longitud del header y longitud total del paquete.
	- Los restantes 0-40 bytes están formados por campos de opciones. 
- **Contenido del encabezado:** Incluye información de enrutamiento IP que los dispositivos utilizan para dirigir el paquete.
- **Tamaño total  del paquete:** Su tamaño máximo es de 65.535 bytes.
# Campos del encabezado 
- **VER (Versión):** 4 bits que indican a los dispositivos receptores qué protocolo usa este paquete.
- **HLEN (Longitud del Encabezado del Paquete):** Indica dónde termina el encabezado del paquete y dónde comienza el segmento de datos.
- **ToS (Type of Service / Tipo de servicio):** Los routers priorizan la entrega de paquetes para mantener la calidad del servicio en la red. El Campo ToS proporciona al router esta Información.
- **Total Length:** Comunica la longitud total de todo el paquete IP, incluye encabezado y datos. Máx. 65.535.
- **Identification:** Los paquetes se subdividen en paquetes más pequeños para ser admitidos por redes cuyo limite es menor a 65.535. El campo de identificación proporciona un identificador único para cada fragmento, para que puedan ser reensamblados cuando lleguen al destino.
- **Flags:** Proporciona al dispositivo de enrutamiento más información sobre si el paquete original ha sido fragmentado y si hay más fragmentos en tránsito.
- **Fragmentation Offset:** indica a los dispositivos de enrutamiento a qué parte del paquete original pertenece el fragmento.
- **TTL (Tiempo de Vida):** El TTL impide que los paquetes de datos sean reenviados por los routers indefinidamente. Contiene un contador que establece la fuente. El contador se decrementa en uno a medida que pasa por cada router a lo largo de su ruta de acceso. Cuando el contador TTL llega a cero, el router que tiene el paquete en ese momento lo descarta y devuelve al remitente un mensaje de error ICMP Time Exceeded.
- **Protocol:** Indica al dispositivo receptor qué protocolo se usará para la parte de datos del paquete.
- **Header to checksum:** Suma de comprobación para detectar si el paquete ha sido corrompido durante el tránsito. Paquetes corruptos se descartan automáticamente.
- **Source IP Address:** Dirección IP de origen.
- **Destination IP Address:** Dirección IP de destino.
- **Options:** El campo de opciones permite aplicar opciones de Seguridad al Paquete si el valor HLEN es superior a cinco. El Campo comunica estas opciones a los dispositivos de enrutamiento.