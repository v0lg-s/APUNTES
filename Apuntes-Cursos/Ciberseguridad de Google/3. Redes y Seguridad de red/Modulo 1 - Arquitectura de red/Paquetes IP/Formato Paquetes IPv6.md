Las direcciones IPv6 están formadas por 8 números hexadecimales separados por ":", cada número tiene hasta cuatro dígitos hexadecimales. En total una dirección IPv6 abarca 16 bytes (IPv4 son 4 bytes) las direcciones IPv6 pueden ser 340 undecilillones (340 seguido de 36 ceros).

Ejemplo: *2002:0db8:0000:0000:0000:ff21:0023:1234.*

_**Nota:**_ para representar uno o más conjuntos consecutivos de todos ceros, puede sustituir los ceros por dos puntos dobles "::", por lo que la dirección IPv6 anterior sería "_2002:0db8::ff21:0023:1234"

![[paqueteIPV6.png]]
- **Versión**: Campo que indica la versión de IP. Para un encabezado IPv6, se utiliza IPv6.
- **Clase de Tráfico**: Este Campo es similar al Campo de Tipo de Servicio IPv4. El Campo de clase de tráfico proporciona información sobre la prioridad o clase del Paquete para ayudar en la entrega del mismo.
- **Etiqueta de Flujo**: Este Campo identifica los paquetes de un Flujo. Un flujo es la secuencia de paquetes enviados desde una fuente específica.
- **Longitud de la carga útil**: Este campo especifica la Longitud de la porción de Datos del paquete.
- **Encabezado siguiente**: Este Campo indica el tipo de Encabezado que sigue al Encabezado IPv6 como TCP.
- **Límite de salto:** Este campo es similar al campo de tiempo de actividad de IPv4. El Límite de Salto limita cuánto tiempo puede viajar un paquete en una red antes de ser descartado.
- **Dirección de origen:** Este Campo especifica la dirección de origen del remitente.
- **Dirección de destino:** Este Campo especifica la dirección de destino del receptor.
