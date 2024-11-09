# CIDR
---
Antes se realizaba el subneteo mediante el sistema de direcciones por clases: 
- A partir de las [[Máscaras de Subred#^da6432|clases]] de direcciones A, B y C se realizaban las subdivisiones de red, es decir, si alguien con una dirección de tipo B cuya cantidad de hosts es de 65.536, deseaba tener 2 subredes dentro de esa dirección de red estaba limitado a tener 256 subredes con capacidad para almacenar 256 hosts *(254 restando la dirección broadcast y la de red)* cada una.

- Se dividía la red en 256, aún cuándo solo se quisiera subdividir en 2.

Para solucionar este problema de eficiencia surgió el *CIDR* (Classless Inter-Domain Routing), este enfoque más moderno y flexible permite obtener divisiones de red más pequeñas sin estar limitado a las clases A, B o C.

- CIDR usa la notación */#* para indicar la cantidad de bits tomados. [[Máscaras de Subred#^6cd642|ver más]]

# Explicación Subnetting de máscara fija
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

