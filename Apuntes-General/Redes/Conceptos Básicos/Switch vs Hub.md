- **Hub:** Cuando recibe una trama de datos hace una copia para todos los dispositivos conectados a sus puertos, es responsabilidad de cada interfaz de red rechazar la trama entrante si no corresponde a su dirección MAC. (Ya son obsoletos)

	- *Colisiones:* Al usar un hub para interconectar varios dispositivos es probable que se generen colisiones entre tramas de datos lo que generará una ralentización considerable.
	- *Velocidad:* La velocidad de la red se ve afectada por la cantidad de dispositivos conectados al hub. (Entre más dispositivos más copias se deben generar, por lo tanto, se produce más tráfico)
	
- **Switch:** Un switch, en principio se comporta como un hub, recibe las tramas y hace una copia a todos los dispositivos, la diferencia radica en que después de la primera comunicación el switch llena una tabla con las direcciones MAC y el puerto (físico en el switch) al que está conectado el dispositivo con esa dirección MAC, de manera que cuando vuelva a recibir una trama de datos, directamente la redirija a su destinatario y no a todos los dispositivos conectados.

	- *Colisiones:* Se reducen casi al mínimo todas las colisiones.
	- *Velocidad:* La velocidad no se reduce por la cantidad de dispositivos conectados, y se mantiene estable.
	- Para mantener la tabla de direcciones MAC actualizada, el switch utiliza la dirección MAC de origen de los paquetes entrantes y el puerto que los paquetes ingresan. La dirección de destino se utiliza para seleccionar el puerto de salida.

- **Router:** Para conectar dos redes separadas se usa un router. El router se conecta al hub o switch de la LAN de ambas redes, usualmente los routers traen un switch integrado. El router se basa en las direcciones IP para realizar el mismo proceso que el switch. Guarda estas direcciones en su tabla de enrutamiento.