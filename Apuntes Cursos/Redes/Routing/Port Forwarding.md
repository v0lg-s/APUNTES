Es una técnica utilizada en redes de computadoras para permitir que el tráfico de datos se dirija desde una puerta de enlace (router o firewall) en la red local hacia un dispositivo específico en la red local, que generalmente se encuentra detrás de ese router o firewall. Esto es útil cuando deseas que ciertos servicios o aplicaciones que se ejecutan en un dispositivo dentro de tu red local sean accesibles desde el mundo exterior a través de Internet.

(Es útil revisar [[NAT#^7db95a|NAT con sobrecarga]])
# Funcionamiento
1. **Necesidad**: Imagina que tienes una cámara de seguridad o un servidor web en tu red local que deseas acceder desde fuera de tu red, como desde Internet. Los dispositivos en Internet necesitan saber cómo llegar a tu dispositivo local, pero tu router actúa como una barrera de seguridad. Por defecto, el router bloquea el acceso desde el exterior para proteger tus dispositivos.
    
2. **Configuración del Router**: Para permitir que el tráfico llegue a tu dispositivo local, debes configurar el router para redirigir ese tráfico hacia el dispositivo específico. Esto se hace a través de la configuración de reenvío de puertos en la interfaz de administración del router.
    
3. **Puertos**: Cada servicio en Internet utiliza puertos específicos para comunicarse. Por ejemplo, el puerto 80 se usa comúnmente para servidores web, el puerto 21 para FTP, y así sucesivamente. Debes especificar el número de puerto que deseas redirigir en la configuración del router.
    
4. **Dirección IP del Dispositivo Local**: Además del número de puerto, también debes especificar la dirección IP interna del dispositivo local al que deseas que llegue el tráfico. Esto asegura que el tráfico se dirija al dispositivo correcto en tu red.
    
5. **Protocolo**: Puedes especificar si deseas redirigir tráfico TCP, UDP o ambos, dependiendo del servicio que estés configurando.
    
6. **Guardar Configuración**: Una vez que hayas configurado el reenvío de puertos en tu router, debes guardar la configuración. Luego, el router se encargará de redirigir el tráfico entrante en el puerto especificado hacia el dispositivo local adecuado.
    
7. **Acceso Remoto**: Ahora, cuando alguien intente acceder a tu cámara de seguridad o servidor web desde Internet, el tráfico llegará primero al router. El router reconocerá la configuración de reenvío de puertos y dirigirá ese tráfico al dispositivo local correcto.

# Puerto Interno vs Externo

- **Puerto externo:** Se refiere al puerto usado en la comunicación desde fuera de la red local, es decir, es el puerto al que las comunicaciones se dirigen cuando están intentando acceder a nuestra red local.
![[puertoExterno.png]]
- **Puerto Interno:** Es el puerto al que se va a redirigir el tráfico dentro de la red, después de pasar por el router y firewall y haber aplicado el proceso de reenvío de puertos. Se refiere al puerto específico que se usará en el dispositivo de destino dependiendo de la aplicación o servicio que se usará.
	- Si se trata de una cámara IP, por lo general, están montadas en servidores web por lo que usarán el puerto 80 para mostrar la información.
	
			192.168.0.1:80

# ¿Cómo Se Realiza?
El reenvío de puertos se configura desde la interfaz web de configuración del router.
![[routerWebInterface.png]]

Se puede realizar también con un rango de puertos, esto sería llamado *Port Range Forwarding*.
