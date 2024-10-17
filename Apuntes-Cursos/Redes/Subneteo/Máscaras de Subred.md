----
# Máscaras de Subred
Sirven para:
- Identificar la red a la que está conectado el [[Roles de Cliente y Servidor#Hosts | host]].
- Distinguir qué parte de una [[Dirección IP | dirección IP]] identifica a la red y qué parte identifica al host. Es decir qué bits corresponden a la red y cuales a los hosts.
- Los hosts usan la máscara de subred para saber si el destino de sus tramas se encuentra en la LAN o en una red remota.

## Máscaras por defecto

*Clase A* → <font color="#BE0000"> 255</font><font color="#43F700">.0.0.0</font> → <font color="#BE0000">RED</font> <font color="#43F700">HOST</font> /8 (Máscara 8) → *8 bits parte de Red → 24 bits parte de Host.*
*Clase B* → <font color="#BE0000"> 255.255</font><font color="#43F700">.0.0</font> → <font color="#BE0000">RED</font> <font color="#43F700">HOST</font> /16 (Máscara 16) → *16 bits parte de Red → 16 bits parte de Host.*
*Clase C* → <font color="#BE0000"> 255.255.255</font><font color="#43F700">.0</font> → <font color="#BE0000">RED</font> <font color="#43F700">HOST</font> /24 (Máscara 24) → *24 bits parte de Red → 8 bits parte de Host.*


**Nota:** No se puede usar 0 ni 255 para identificar a un host porque son exclusivas de la red y la dirección broadcast respectivamente. ^eabba1
- La notación *"/#"* se usa para indicar de que máscara de red se trata sin tener que decir la dirección completa. El número indica la cantidad de 1's en los [[Dirección IP#Características|octetos]] de la dirección IP. Este número indica la cantidad de bits usados en la dirección IP para identificar la red. ^6cd642
### Rangos de Clases de Red

| Clase de dirección | Rango del primer octeto | Notación /# |     Mascara de subred      |         Numero de posibles redes y hosts por red         | Rango en binario                                                      |
| ------------------ | :---------------------: | :---------: | :------------------------: | :------------------------------------------------------: | --------------------------------------------------------------------- |
| Clase A            |          0-127          |     /8      |         255.0.0.0          |         128 redes. <br>$$2^{24}-2\text{ Hosts}$$         | <font color="red">0</font>0000000 - <font color="red">0</font>1111111 |
| Clase B            |         128-191         |     /16     |        255.255.0.0         | $$2^{14}\text{ Redes}$$<br>$$2^{16}-2\text{ Hosts}$$<br> | <font color="red">10</font>000000 - <font color="red">10</font>111111 |
| Clase C            |         192-223         |     /24     |       255.255.255.0        |   $$2^{21}\text{ Redes}$$ $$2^{8}-2\text{ Hosts}$$<br>   | <font color="red">110</font>00000 - <font color="red">110</font>11111 |
| Clase D            |         224-239         |             |  Es usada para multicast.  |                                                          | 111                                                                   |
| Clase E            |         240-255         |             | Es usada para experimentar |                                                          | 1111                                                                  |
## Cómo se forman las máscaras de red

Para formar una mascara de red se comienza encendiendo los bits de la dirección desde la izquierda.

	100000000.00000000.00000000.00000000

La anterior sería la primer máscara de subred es decir */1*. Al convertirla en decimal se obtiene:

	128.0.0.0

Todas las máscaras de red se forman de esta manera por lo que como máximo podemos obtener la mascara */32*.

	 11111111.11111111.11111111.11111111

^0b750b

Cada vez que encendemos un bit hacia la derecha se subdivide la red original. En la tabla es posible ver la cantidad de hosts por cada subdivisión.

Por esta razón los posibles valores decimales que puede tomar cada octeto en una mascara de red son:
1. 0, 128, 192, 224, 240, 248, 252, 254, 255

![[mscaras_subred.png|500]] ^da6432