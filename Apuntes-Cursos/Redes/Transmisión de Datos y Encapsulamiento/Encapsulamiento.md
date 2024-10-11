Se refiere al *proceso de empaquetar datos en capas sucesivas*, donde cada capa agrega su propia información y encabezados antes de enviar los datos a través de una red o de otro sistema. A medida que avanza la comunicación *cada capa de red agrega un encabezado con información específica del protocolo que funcione en dicha capa*. A este proceso se le llama *encapsulamiento*.

==Todo este proceso sucede en el dispositivo emisor.==

En el dispositivo receptor sucede el proceso contrario, el *des encapsulamiento*

Por ejemplo, en el modelo de referencia OSI, que consta de siete capas, el proceso de encapsulamiento se da de la siguiente manera:

1. **Capa de Aplicación**:
    - Los datos de la aplicación (por ejemplo, un archivo, una solicitud HTTP) se preparan para su transmisión.
    - Se agrega un encabezado que contiene información de la capa de aplicación (como puertos de origen y destino).
1. **Capa de Presentación**:
    - Los datos de la capa de aplicación se encapsulan en un formato adecuado para la transmisión.
    - Puede haber cifrado, compresión u otras transformaciones de datos.
    - Agrega detalles como la codificación y el formato de los datos.
2. **Capa de Sesión**:
    - Los datos de la capa de presentación se encapsulan en un formato de sesión.
    - Se agrega información para el establecimiento, mantenimiento y cierre de sesiones.
3. **Capa de Transporte**:
    - Los datos de la capa de sesión se encapsulan en segmentos (en [[Protocolo TCP#TCP (Transmission Control Protocol)|TCP]]) o datagramas (en [[Protocolo TCP#UDP (User Datagram Protocol)|UDP]]).
    - Se agrega un encabezado que contiene información de la capa de transporte (como números de puerto de origen y destino).
4. **Capa de Red**:
    - Los segmentos o datagramas de la capa de transporte se encapsulan en paquetes IP.
    - Se agrega un encabezado que contiene información de la capa de red (como direcciones IP de origen y destino).
5. **Capa de Enlace de Datos**:
    - Los paquetes IP se encapsulan en tramas de enlace de datos (como tramas Ethernet).
    - Se agrega un encabezado que contiene información de la capa de enlace de datos (como direcciones MAC de origen y destino).
6. **Capa Física**:
    - Las tramas de enlace de datos se convierten en señales eléctricas, ópticas u otras formas para la transmisión a través del medio físico de la red.

![[encapsulamiento.png]]
El último encabezado es el de la capa de enlace, en esta capa la trama puede ser una trama ethernet (si se trata de una trama que viaja solamente en la [[Tipos de Redes#Redes Locales|LAN]]) o un paquete (si se trata de una trama que saldrá de su LAN).
![[capsula.png]]

# Unidad de datos del protocolo (PDU)
En el proceso de encapsulación, la forma que adopta una porción de datos en cualquier capa de modelo se denomina Unidad de Datos del Protocolo.
En cada etapa una PDU tiene un nombre distinto para reflejar sus nuevas funciones.
- *Datos:* Capa de aplicación.
- *Segmento:* Capa de transporte.
- *Paquete:* Capa de red.
- *Trama:* Capa de enlace de datos.
- *Bits:* Capa física.