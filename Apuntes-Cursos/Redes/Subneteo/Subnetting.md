El subnetting, es una técnica utilizada en redes de computadoras para dividir una red IP física en subredes lógicas (más pequeñas), para que cada una de estas trabaje a nivel de envío y recepción de paquetes como una red individual aunque todas pertenezcan a la misma red.

Permite una *mejor administración, control de tráfico y seguridad* al segmentar la red por función.
Sería una falla de seguridad tener todos los dispositivos en una red grande ya que un intruso en la red podría ver y monitorear lo que hacen otros dispositivos. 

*Por ejemplo*, una red de una universidad debería subdividir su red en una red para estudiantes, profesores y una de invitados de manera que cada persona se mantenga dentro de la red de su rol y no pueda acceder a dispositivos conectados a alguna de las otras subredes.

Como *desventaja*, su implementación desperdicia muchas direcciones.

- Para realizar estas subdivisiones se usa un sistema llamado CIDR - Classless Inter-Domain Routing.
- Las máscaras de subred tienen todos los 1's a la izquierda y todos los 0's a la derecha.
- Entre más subredes se creen menos hosts se pueden conectar a cada subred.

# CIDR
---
Antes se realizaba el subneteo mediante el sistema de direcciones por clases: 
- A partir de las [[Máscaras de Subred#^da6432|clases]] de direcciones A, B y C se realizaban las subdivisiones de red, es decir, si alguien con una dirección de tipo B cuya cantidad de hosts es de 65.536, deseaba tener 2 subredes dentro de esa dirección de red estaba limitado a tener 256 subredes con capacidad para almacenar 256 hosts *(254 restando la dirección broadcast y la de red)* cada una.

- Se dividía la red en 256, aún cuándo solo se quisiera subdividir en 2.

Para solucionar este problema de eficiencia surgió el *CIDR*, este enfoque más moderno y flexible permite obtener divisiones de red más pequeñas sin estar limitado a las clases A, B o C.

- CIDR usa la notación */#* para indicar la cantidad de bits tomados. [[Máscaras de Subred#^6cd642|ver más]]
## Funcionamiento 
---
- Se basa en entender que las direcciones IP en binario en realidad no están divididas en octetos sino que es una secuencia completa de 1's y 0's sin puntos separándolas.

		11111111.11111111.11111111.00000000
	
- El computador en realidad vería lo anterior como:

		11111111111111111111111100000000

- Siguiendo este principio, no es necesario hacer máscaras de red para subredes saltando entre cada octeto, sino que por el contrario se podía tomar la cantidad de bits que se necesitan de cada octeto.

# Explicación Subnetting
---
Para este ejemplo es necesario ver [[Máscaras de Subred#^da6432|Tabla de máscaras de red]]
- Tenemos la dirección IP de una red <font color = "#F2D923">208.25.160.0</font>, esta dirección es de clase C ([[Máscaras de Subred#Rangos de Clases de Red|ver rangos de clases]]), por lo que su máscara de red es <font color = "#F2A423">255.255.255.0</font>. En binario:
	- <font color = "#F2D923">11010000.00011001.10100000.00000000</font> → Dirección IP
	- <font color = "#F2A423">11111111.11111111.11111111.00000000</font> → Máscara de subred /24
- Al "correr" o "tomar prestado" un bit a la derecha de la máscara de subred. Obtenemos:
	- <font color = "#F2A423">11111111.11111111.11111111.<font color = "red">1</font>0000000</font> → Máscara de subred /25
	- <font color = "#F2A423">255.255.255.128</font> → Máscara de subred /25
- La dirección IP en ese bit puede tomar 2 posibles valores "1" o "0" y obtener una subred con un rango de direcciones IP para hosts de:
	- <font color = "#F2D923">11010000.00011001.10100000.<font color = "red" >0</font><font color = "green" >0000001</font></font> *→ 208.25.160.1*
	- <font color = "#F2D923">11010000.00011001.10100000.<font color = "red" >0</font><font color = "green" >1111110</font></font> *→ 208.25.160.126*
- Y una segunda subred en un rango de direcciones IP para hosts de:
	- <font color = "#F2D923">11010000.00011001.10100000.<font color = "red" >1</font><font color = "green" >0000001</font></font> *→ 208.25.160.129*
	- <font color = "#F2D923">11010000.00011001.10100000.<font color = "red" >1</font><font color = "green" >1111110</font></font> *→ 208.25.160.254*

*Recordar:* ![[Máscaras de Subred#^eabba1]]
En este caso no se usan de:
**La subred 1:** 
→ 208.25.160.0 porque esta dirección identifica la subred 1. *→ Primera dirección*
→ 208.25.160.127 porque esta dirección es la dirección de broadcast. *→ Última dirección*

**La subred 2:**
→ 208.25.160.128 porque esta dirección identifica la subred 2.  *→ Primera dirección*
→ 208.25.160.255 porque esta dirección es la dirección de broadcast. *→ Última dirección*

# Calculo de Subredes

A partir de la dirección IP dada tenemos que ver de que clase es dependiendo de su rango:
![[Máscaras de Subred#Rangos de Clases de Red]]

Una vez conocemos a qué clase pertenece esta dirección podemos saber cual es su máscara de red predeterminada, es con esta máscara de red en binario que trabajaremos para realizar el subneteo.

--- 
**Cantidad de subredes según los dígitos tomados del octeto:**
En el subneteo según la cantidad de dígitos binarios tomemos del octeto de host en la máscara original obtendremos la cantidad de subdivisiones que se realizarán:
- **1 Bit → 2 subredes** → 2<sup>1</sup> = 1
- **2 Bits → 4 subredes** → 2<sup>2</sup> = 4

Por lo que, sea x→ cantidad de bits
- $2{^{x}}=$  ==Cantidad de subredes con x bits.==

Si nos dan un requerimiento de cantidad de subredes a partir de una dirección IP, debemos tener en cuenta las potencias de 2, *Por ejemplo* si nos piden dividir una red en 29 subredes tendremos que usar 5 bits ya que:
- $2{^5}=32$ subredes  
![[potencias.gif]]


*Tener en cuenta* que si la cantidad de subredes requeridas no es una potencia de 2 tendremos que aproximarla a la potencia mayor más cercana.

---

## Ejemplo Calculo de Subredes

Usemos la dirección de clase C 192.190.0.0 cuya máscara de subred es 255.255.255.0 /24 o en binario:

	11111111.11111111.11111111.00000000 /24

==Se solicita tener 3 subredes.==

A partir de las potencias de 2 sabemos que la cantidad de bits necesarios en el último octeto para dividir la red en 3 subredes es 2. *→* $2{^2}=4$

Es por esto que la máscara de red debe tener dos bits en "1" en el octeto de host.

	11111111.11111111.11111111.11000000 /26

En decimal, <font color = "#F2A423">255.255.255.192</font> /26.

En principio la máscara de subred 255.255.255.0 tenía la posibilidad de contener 256 hosts (son las posibles combinaciones de los bits en 0 del último octeto) en una sola red, ahora que se dividió la red en 4, obtenemos:

$$
\large {\frac{256 \text{ Hosts totales}}{4 \text{ subredes}}=64 \text{ Hosts por red}}
$$

También podríamos haberlo calculado con la cantidad de 0's que son la parte de host de la mascara de subred, en este caso son 6 "0's" y se calcularían las posibles combinaciones así:

$$
2^{6} = 64 \text{ combinaciones posibles o hosts por red}
$$

Por lo tanto, el incremento de la dirección IP es de 64 y los rangos en las 4 subredes serán así:

**Subred 1:**
- 192.190.0.0 → Inicio *Dirección de red*
- 192.190.0.63 → Final *Dirección de Broadcast*
**Subred 2:**
- 192.190.0.64 → Inicio *Dirección de red*
- 192.190.0.127 → Final *Dirección de Broadcast*
**Subred 3:**
- 192.190.0.128 → Inicio *Dirección de red*
- 192.190.0.191 → Final *Dirección de Broadcast*
**Subred 4:**
- 192.190.0.192 → Inicio *Dirección de red*
- 192.190.0.255 → Final *Dirección de Broadcast*

*Recordar,* las direcciones de red y broadcast NO pueden ser asignadas a hosts de la red.
*Notemos* que la dirección de inicio de cada red es la suma del incremento "64" para este caso, en la parte de host de la dirección de la subred anterior. Además nos sobra una red teniendo en cuenta el requerimiento.