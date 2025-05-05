**Tener en cuenta:** Es un escaneo lento ya que completa la conexión con el objetivo y después la interrumpe para determinar el estado de los puertos, además puede dejar rastros en los logs de conexión.

---
**Switch**
```bash
nmap -sT 
```
Es importante recordar el funcionamiento del [[Protocolo TCP#Three-Way Handshake|Three Way Handshake]] que desempeña el protocolo TCP. Este tipo de escaneo efectúa el [[Protocolo TCP#Three-Way Handshake|Three Way Handshake]] en cada uno de los puertos a escanear en el objetivo.

![[TCP-Connect.png]]
Es decir, para determinar el estado de un puerto este escaneo se intenta conectar al puerto, durante este proceso existen 3 posibilidades:

1. **Puerto cerrado:** Si el puerto está cerrado el servidor objetivo responderá con un paquete TCP con la flag RST seteados.
2. **Puerto abierto:** Si el puerto está abierto la maquina responderá con un paquete TCP con SYN/ACK seteados. A lo que nuestra maquina responderá con un TCP ACK para confirmar la conexión. (Tras esto tendrá que cerrarla de nuevo con RST).
3. **Puerto Filtrado/Abierto:** Puede que el puerto este abierto pero detrás de un firewall, usualmente los firewalls se configuran para descartar paquetes entrantes, por lo que en este caso, no habrá ninguna respuesta y se considera al puerto como filtrado/abierto.

**Nota:** Si se configura un firewall para que en vez de descartar un paquete entrante lo responda con un paquete TCP RST nos dará una lectura errónea en el escaneo. (Buena táctica anti escaneos) 

**Revisar** Podemos revisar el estándar RFC 9293 para ver el comportamiento de TCP.