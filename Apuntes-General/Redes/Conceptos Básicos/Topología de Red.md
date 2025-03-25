
# Topología Física
Identifica la ubicación de los dispositivos, la disposición física de los cables y cómo los dispositivos están conectados entre sí. Define la estructura física real de la red.

## Topología de Bus
Todos los dispositivos están conectados a un único cable principal.
- **Ancho de banda:** Todos los hosts comparten el ancho de banda, en este caso, si hay muchos dispositivos conectados a la red será más lenta.
- **Transmisión:** Los datos se transmiten por el cable principal y todos los hosts lo escuchan pero solo el destinatario lo procesa.
![[Bus-topologia.png|600]]
## Topología de anillo
Los dispositivos están conectados formando un circulo cerrado. Cada dispositivo se conecta a dos dispositivos vecinos y los datos se transmiten a los largo del anillo en una dirección.
- **Funcionamiento:** Funciona con un token, solo el equipo con el token puede enviar información, por lo tanto, solo un dispositivo puede enviar información al tiempo.
- **Fallas:** Si un dispositivo se daña se pierde la conexión entre todos.

![[Red_Anillo.png|350]]
## Topología de Estrella 
Cada dispositivo se conecta a un punto central, como un conmutador.
- **Transmisión:** La transmisión y comunicación se da por medio del punto central, los datos son transmitidos a este punto central y este los redirige a su destino.
- Es muy común.
- **Ancho de Banda:** Solo se limita por la capacidad del punto central.

![[estrella-red.png|350]]

## Topología de Malla
Cada dispositivo está conectado a todos los demás.
- Puede ser costoso y complejo en términos de cableado.
- Proporciona tolerancia a fallas.
- Es práctico en escenarios de redes inalámbricas.
![[malla-red.png]]