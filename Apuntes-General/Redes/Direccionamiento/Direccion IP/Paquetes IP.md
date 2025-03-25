
Cuando un computador se quiere comunicar con otro en una red distinta la trama de datos se modifica en la capa de red:
- *Dirección MAC de Destino:* La trama Ethernet incluye la dirección MAC del dispositivo de origen (fuente) y la dirección MAC del router (puerta de enlace) de la red externa como destino. 
## Empaquetamiento
- *Dirección IP de Destino:* El dispositivo transmisor reconoce que la dirección IP de destino no pertenece a su red, por lo que usa la puerta de enlace predeterminada ==(Default Gateway)== que es la dirección que siempre apunta al router.
- *Dirección IP de Origen:* Es la dirección IP del dispositivo transmisor.

# Como Viaja la Trama de Datos con Direccionamiento IP
Cuando los datos viajan entre redes distintas utilizando direccionamiento IP, se requiere que las direcciones MAC y las direcciones IP trabajen juntas para asegurar que los datos sean correctamente direccionados y entregados a través de las diferentes redes. El proceso de modificar la trama de Ethernet para el enrutamiento entre redes se conoce como encapsulación y des encapsulación.

Aquí está el proceso básico de cómo ocurre este proceso:

1. **Encapsulación en la red de origen:**
    - Supongamos que un dispositivo en una red A desea enviar datos a un dispositivo en una red B utilizando direcciones IP.
    - El dispositivo de origen encapsula los datos en una trama Ethernet.
    - La trama Ethernet incluye la dirección MAC del dispositivo de origen (fuente) y la dirección MAC del router (puerta de enlace) de la red A como destino.
2. **Enrutamiento en el router:**
    - La trama Ethernet llega al router que conecta la red A con la red B.
    - El router desencapsula la trama Ethernet y examina la dirección IP de destino.
    - El router determina la mejor ruta para el paquete en función de su tabla de enrutamiento y decide hacia qué red enviará el paquete.
3. **Encapsulación en la nueva red:**
    
    - El router encapsula los datos en una nueva trama Ethernet para la red B.
    - La trama Ethernet incluye la dirección MAC del router en la red B como fuente y la dirección MAC del dispositivo de destino en la red B como destino.
4. **Entrega en la red de destino:**

    - La trama Ethernet encapsulada llega a la red B y es entregada al dispositivo de destino.
    - El dispositivo de destino desencapsula la trama Ethernet para acceder a los datos originales.