![[puertos-PROTOCOLOS.png]]
# UDP (User Datagram Protocol)
UDP es un protocolo sin conexión y no confiable en comparación con TCP. Se caracteriza por ser más ligero y rápido, pero no ofrece garantías de entrega ni ordenación de los datos. (no orientado a conexión).

No establece una conexión por lo que se envían datos sin saber si se van a recibir.

En UDP, los datos se envían en forma de datagramas independientes sin establecer una conexión previa ni confirmar la entrega. No hay un proceso formal de apretón de manos o sincronización en UDP, ya que no se mantiene un seguimiento de números de secuencia ni se espera reconocimientos de recibos.
- *No confiable:* 
	- No hace una recuperación de errores o confidencialidad.

## Uso
El encabezado UDP no es tan grande como el TCP por lo que no se deben usar más recursos y más bytes introducidos en la trama de datos a diferencia de TCP.

**Aplicaciones adecuadas:** UDP es comúnmente utilizado para aplicaciones como streaming de video, llamadas VoIP, juegos en línea y servicios de transmisión en tiempo real, en donde no importa si se pierden paquetes en el camino.