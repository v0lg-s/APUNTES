**Tener en cuenta** Es el mejor escaneo, siempre que esté disponible debemos usar este tipo. Es considerado, poco ruidoso y no deja rastro ya que no completa las conexiones.

Se debe realizar con permisos de SU.

---
**Switch**
```bash
nmap -sS
```

Este tipo de escaneo realiza el proceso del [[Protocolo TCP#Three-Way Handshake|Three Way Handshake]] hasta la mitad, se ilustra mejor en una imagen, pero, cuando la maquina responde con un paquete TCP SYN/ACK nuestra maquina ya puede determinar el estado de ese puerto, y antes de terminar el proceso envía un TCP RST para dejar la conexión a medias. (Por eso también se le llama Half-open scan)

![[half-connect-TCP.png]]

**Posibles respuestas:** Son iguales a un [[TCP Connect Scan]]
1. **Puerto cerrado:** Si el puerto está cerrado el servidor objetivo responderá con un paquete TCP con la flag RST seteada.
2. **Puerto abierto:** Si el puerto está abierto la maquina responderá con un paquete TCP con SYN/ACK seteados. A lo que nuestra maquina responderá con un TCP RST.
3. **Puerto filtrado/abierto:** No hay respuesta o se envenena con un TCP RST.

**Por qué es la mejor opción?**
- Puede ser usado para evadir [[Sistemas De Detección y Prevención#IDS (Sistema de Detección de Intrusiones)|IDS]] antiguos que buscan patrones en los three way handshakes completos.
- Las practicas estándar de logs es registrar las conexiones completas, por lo tanto, este tipo de escaneo no es registrado en los logs.
- Es significativamente más rápido por no completar las conexiones.