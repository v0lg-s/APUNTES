El subnetting, es una técnica utilizada en redes de computadoras para dividir una red IP física en subredes lógicas (más pequeñas), para que cada una de estas trabaje a nivel de envío y recepción de paquetes como una red individual aunque todas pertenezcan a la misma red.

Permite una *mejor administración, control de tráfico y seguridad* al segmentar la red por función.
Sería una falla de seguridad tener todos los dispositivos en una red grande ya que un intruso en la red podría ver y monitorear lo que hacen otros dispositivos. 

*Por ejemplo*, una red de una universidad debería subdividir su red en una red para estudiantes, profesores y una de invitados de manera que cada persona se mantenga dentro de la red de su rol y no pueda acceder a dispositivos conectados a alguna de las otras subredes.

Como *desventaja*, su implementación desperdicia muchas direcciones.

- Para realizar estas subdivisiones se usa un sistema llamado CIDR - Classless Inter-Domain Routing.
- Las máscaras de subred tienen todos los 1's a la izquierda y todos los 0's a la derecha.
- Entre más subredes se creen menos hosts se pueden conectar a cada subred.

## Funcionamiento 
---
- Se basa en entender que las direcciones IP en binario en realidad no están divididas en octetos sino que es una secuencia completa de 1's y 0's sin puntos separándolas.

		11111111.11111111.11111111.00000000
	
- El computador en realidad vería lo anterior como:

		11111111111111111111111100000000

- Siguiendo este principio, no es necesario hacer máscaras de red para subredes saltando entre cada octeto, sino que por el contrario se podía tomar la cantidad de bits que se necesitan de cada octeto.




