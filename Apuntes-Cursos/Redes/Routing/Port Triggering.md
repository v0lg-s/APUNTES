Se usa usualmente con el protocolo FTP, ya que cuando un dispositivo hace una petición a un servidor FTP usualmente lo hace mediante el puerto 21, cuando el servidor responde este puede responder por el puerto 20 o 21 por lo que el router cuando haga uso de [[NAT#^7db95a|NAT]] no entenderá a qué dispositivo se dirige esa información.

![[port-Triggering.png]]

Para solucionar esto se hace uso del *Port Triggering* especificando que si una comunicación es establecida mediante el puerto 21 al momento de salir de la LAN, entonces los servicios pueden responder mediante los puertos 20-21.