El ataque DoS (Denial of Service)/ ataque de denegación de servicios es un ataque que afecta redes o servidores y los inunda con tráfico de red.
- Enviar una cantidad tan grande de solicitudes o tráfico que el servidor o la red sea incapaz de responder a las solicitudes legitimas o en absoluto siquiera responder.

Una variante muy común de este ataque es el **ataque DDoS** (Denegación de Servicio Distribuido) es un tipo de DoS que usa múltiples dispositivos o servidores en locaciones distintas (usualmente se trata de una botnet) para inundar la red objetivo con tráfico no deseado.

# Tipos de ataque DoS

## Ataque de inundación SYN
Es un tipo de ataque DoS que simula una conexión TCP e inunda el servidor con paquetes SYN. 
**Nota:** Útil revisar: [[Protocolo TCP]]

## Ataque de inundación ICMP
Tipo de ataque DoS dónde el atacante envía repetidamente paquetes ICMP al servidor de una red.
Esto fuerza al servidor a enviar un paquete ICMP, eventualmente esto usa todo el ancho de banda y colapsa todo el servidor.

## Ping de la muerte
Es un tipo de ataque DoS que se da cuando un hacker hace ping a un sistema enviándole un paquete ICMP sobredimensionado que pesa más de 64KB (Máximo tamaño de un paquete ICMP).