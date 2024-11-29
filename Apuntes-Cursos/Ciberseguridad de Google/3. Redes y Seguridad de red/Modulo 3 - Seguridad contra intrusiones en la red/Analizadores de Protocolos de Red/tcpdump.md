Es un analizador de protocolos de red de línea de comandos, es decir, no tiene una interfaz gráfica que nos permita interactuar con los registros. Es popular por varias razones:
- Es ligero, usa poca memoria y bajo uso de CPU.
- Utiliza la biblioteca de código abierto libpcap.
- Todos los comandos de tcpdump se ejecutan en la terminal.
- Se puede instalar en otros sistemas operativos basados en Unix, como MacOS.
- Viene preinstalado en varias distribuciones de Linux.

Tcpdump proporciona un breve análisis de paquetes y convierte la informacíon clave sobre el tráfico de red en formatos fácilmente legibles por humanos.
- La información de cada paquete la imprime en la terminal.
- Muestra la dirección IP de origen y destino.
- Muestra los números de puerto que se están utilizando en las comunicaciones.

## ¿Cómo leer los registros?
Puede imprimir la información de los paquetes olfateados en la línea de comandos y opcionalmente en un archivo. Así se ve una salida de un paquete olfateado:
![[salidaTcpdump.png]]
**Explicación:**
- **Timestamp o Marca de Tiempo:**  La salida comienza con la marca de tiempo, formateada como horas, minutos, segundos y fracciones de segundo.
- **Source IP/IP de Origen:** Origen del paquete.
- **Puerto de origen:** Número de puerto de dónde se originó el paquete.
- **IP de destino:** La dirección IP de destino del paquete.
- **Puerto de destino:** Número de puerto hacia dónde se está transmitiendo el paquete.

**Nota:** Por defecto, tcpdump intentará resolver las direcciones de host a nombres de host. También sustituirá los números de puerto por servicios comúnmente asociados que utilicen estos puertos.