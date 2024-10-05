---

---
-----
![[puertos-PROTOCOLOS.png]]
# TCP (Transmission Control Protocol)
TCP es un protocolo orientado a la conexión y confiable. Es un protocolo de la [[Modelo OSI#Capa 4 Capa de Transporte|capa de transporte]] que se centra en garantizar que los datos se entreguen de manera ordenada, completa y sin errores a través de una conexión establecida entre el remitente y el receptor.

Se encarga de establecer la conexión entre 2 computadores antes de realizar el envío de datos, así mismo, cuando finaliza la transmisión de datos TCP termina la conexión entre las computadoras.
- Así como la trama de datos viene con un encabezado desde su origen, a medida que avanza la comunicación cada capa de red agrega un encabezado, cuando se llega a la ==capa de transporte== el protocolo TCP agrega un encabezado.
- **Controla el Flujo de Datos**, es decir, monitorea teniendo en cuenta la velocidad de transmisión para no saturar la red.
	- *Por ejemplo*, Si el receptor está ocupado, el remitente reduce la velocidad de envío.
- **Controla la Congestión**, es decir, maneja la congestión en la red ajustando la velocidad de transmisión según la carga de la red. Esto evita que se saturen los enlaces y se produzcan problemas de rendimiento.
- Garantiza:
	- ==Flujo==
	- ==Orden==
	- ==Llegada al Destino==
## Encabezado TCP

![[encabezado-TCP.png]]

- *Source Port:* La computadora revisa qué puerto tiene libre y lo reserva para su uso y lo escribe en este campo.
- *Destination Port:* Dependiendo del tipo de comunicación que se realiza, se escoge el puerto en el destino.
	- *Ejemplo:* Si se trata de una comunicación con un sitio web, se enviarán los datos al puerto 80 del dispositivo receptor.
- *Sequence Number:* Permite reensamblar la información en dado caso se haya fragmentado en varios trozos a cargo del software de red, proporciona una secuencia en los paquetes para que este software sepa qué trozos o paquetes vienen en qué orden.
- *Acknowledgement Number:* Le comunica al otro computador que se recibió la información.
### Flag Bits
Se hace uso de varias banderas para comunicar un estado en la conexión y comunicación (2 bits). Existen 9 pero las mas usadas son 6. Entre ellas se encuentran:
#### SYN
Se utiliza para ==iniciar una conexión entre dos hosts.== Cuando un host desea establecer una conexión TCP, envía un segmento con la bandera SYN activada. El mensaje indica que el remitente quiere sincronizar los números de secuencia para establecer la conexión. (Inicia la Conexión)
#### ACK
Esta bandera se utiliza para ==confirmar la recepción exitosa de datos.== (Inicia la Conexión)
Si el remitente no recibe un ACK en un tiempo determinado, retransmite los datos para garantizar la entrega.
#### RST 
Esta bandera se utiliza para ==reiniciar una conexión TCP abruptamente.== Cuando un host envía un segmento con la bandera RST activada, está indicando que la conexión debe ser restablecida y cualquier flujo de datos pendiente debe ser interrumpido. (Aborta la Conexión)
#### FIN
Indica que ==el remitente ha terminado de enviar datos y quiere cerrar la conexión.== Cuando un host envía un segmento con la bandera FIN activada, indica que ya no enviará más datos. (Aborta la Conexión)
#### PUSH 
Esta bandera se usa para ==indicar al receptor que debe entregar los datos recibidos a la capa superior (aplicación) inmediatamente, en lugar de acumularlos en un búfer (Transferencia de Datos)==
#### URG 
Se utiliza para ==indicar que los datos contenidos en el segmento son urgentes y requieren un manejo especial.== Esto es útil para situaciones en las que ciertos datos necesitan ser procesados antes que otros. (Transferencia de Datos)

## Three-Way Handshake
Antes que TCP transmita información, usará un proceso conocido como "Three-Way Handshake" para establecer una conexión. Es un proceso realizado al inicio de una comunicación y asegura que ambos dispositivos estén sincronizados. Consta de tres pasos:
El dispositivo que inicia la conexión será llamado "cliente", el dispositivo receptor "servidor".

1. **Paso SYN:** El cliente envía un segmento TCP con la bandera *SYN* activada al servidor solicitando sincronización. El segmento contiene un número de secuencia inicial elegido por el cliente. Este número de secuencia se utiliza para rastrear los datos enviados y recibidos durante la conexión.
	- "Hola servidor, ¿puedes abrir una conexión para mí?"
2. **Paso SYN-ACK:** El servidor envía un segmento TCP con las banderas *SYN* y *ACK* activadas. El servidor también elige un número de secuencia inicial y un número de reconocimiento *(ACK)* que es el número de secuencia del cliente incrementado en uno.
	- "Hola cliente, sí abriré una conexión para ti. ¿puedes tú abrir una conexión para mi?"
3. **Paso ACK:** Finalmente, el cliente envía un tercer segmento TCP con la bandera *ACK* activada. El número de secuencia en este segmento es incrementado en uno a partir del número de reconocimiento *(ACK)* del servidor.
	- "Claro!"

![[three way handshake.png]]


