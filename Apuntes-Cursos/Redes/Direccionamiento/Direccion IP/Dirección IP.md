Ya que las direcciones MAC no identifican que un grupo de computadores pertenecen a una [[Tipos de Redes#^4b7544|red local]] específica se hacen necesarias las direcciones IP para identificar redes y dispositivos al tiempo.

Como lo dice su nombre una dirección IP es literalmente una dirección (número) que identifica un dispositivo en internet. Así como una casa en una ciudad tiene una dirección para saber cómo llegar, un dispositivo en internet tiene su dirección IP única.

- Son usadas para el enrutamiento y segmentación:
	- **Enrutamiento de datos:** En redes de mayor escala, como Internet, los datos deben ser enviados a través de múltiples nodos intermedios antes de llegar a su destino final. Las direcciones IP permiten que los routers y otros dispositivos de red identifiquen el camino correcto para enrutar los datos hacia su destino.
	- **Segmentación de redes:** Las redes grandes pueden dividirse en segmentos más pequeños para facilitar la administración y mejorar el rendimiento. Cada segmento puede tener su propio rango de direcciones IP, lo que ayuda a mantener el orden y la organización en la red. (Ver [[Subnetting | subnetting]])
- Es un requisito para conectarse a internet para que otros dispositivos puedan enviar y recibir datos de el dispositivo.

# Características
- No están fijadas a una tarjeta de red específica.
- Son únicas.
- Se puede usar para identificar una red en particular.
- Pueden cambiar.
- Son números entre 0-255.
Una dirección IP luce así después de ser convertida al sistema decimal:  

		192.168.1.1

Son escritas como 4 octetos binarios.

		11000000.10101000.00000001.00000001

 Los primeros tres números, es decir, ==192.168.1== identifican a la red. El último número identifica al dispositivo conectado a esa red. Lo anterior teniendo en cuenta la [[Máscaras de Subred | máscara de red]].
*Nota:* En realidad el computador no tiene los puntos que dividen los octetos, son notaciones para facilitar la lectura.

