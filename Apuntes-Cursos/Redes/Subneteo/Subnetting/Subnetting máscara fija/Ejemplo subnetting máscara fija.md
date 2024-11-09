
Usemos la dirección de clase B 150.12.0.0 cuya máscara de subred es 255.255.0.0 /16 o en binario:

	11111111.11111111.00000000.00000000 /24

==Se solicita tener 3 subredes.==

A partir de las potencias de 2 sabemos que la cantidad de bits necesarios en el siguiente octeto para dividir la red en 3 subredes es 2. *→* $2{^2}=4$

Es por esto que la máscara de red debe tener dos bits en "1" en el octeto de host.

	11111111.11111111.11000000.00000000 /18

En decimal, <font color = "#F2A423">255.255.192.0</font> /18.

En principio la máscara de subred 255.255.0.0 tenía la posibilidad de contener 65.536 hosts (son las posibles combinaciones de los bits en 0 del último octeto) en una sola red, ahora que se dividió la red en 4, obtenemos:

$$
\large {\frac{65.536 \text{ Hosts totales}}{4 \text{ subredes}}=16.384 \text{ Hosts por red}}
$$

También podríamos haberlo calculado con la cantidad de 0's que son la parte de host de la mascara de subred, en este caso son 14 "0's" y se calcularían las posibles combinaciones así:

$$
2^{14} = 16.384 \text{ combinaciones posibles o hosts por red}
$$

Para conocer los rangos de las direcciones IP de las subredes podemos usar el siguiente método:
1. A partir de la máscara de subred nueva, podemos definir los rangos en los octetos.
	1. <font color = "#F2D923">11111111.11111111.<font color = "red" >11000000.</font><font color = "green" >00000000</font></font>
2. En rojo está el octeto del que se "descompletaron" los 0's y que por lo tanto su rango ha cambiado. Tomamos la cantidad de 0's restantes de este octeto y calculamos las posibles combinaciones, es decir:
$$
2^{6} = 64 \text{ combinaciones posibles}
$$
3. Encontramos que el salto en este octeto es de 64 en 64. 
4. Las **direcciones de red** de cada subred se encontrarán dando esos saltos de 64 en este octeto.
5. Para calcular las **direcciones de Broadcast**, simplemente nos devolvemos una dirección de la siguiente subred.
6. Para el **primer host de una subred**, es una dirección siguiente a la dirección de red de dicha subred.
7. Para el **último host de una subred**, es una dirección antes a la dirección de broadcast de dicha subred.

| **# Subred** | **Dirección de red** | **Dirección de Broadcast** | **Primer Host** | **Último Host** |
| :----------: | :------------------: | :------------------------: | :-------------: | :-------------: |
|      0       |      150.12.0.0      |       150.12.63.255        |   150.12.0.1    |  150.12.63.254  |
|      1       |     150.12.64.0      |       150.12.127.255       |   150.12.64.1   | 150.12.127.254  |
|      2       |     150.12.128.0     |       150.12.191.255       |  150.12.128.1   | 150.12.191.254  |
|      3       |     150.12.192.0     |       150.12.255.255       |  150.12.192.1   | 150.12.255.254  |

*Recordar,* las direcciones de red y broadcast NO pueden ser asignadas a hosts de la red.
*Notemos* que la dirección de inicio de cada red es la suma del incremento "64" para este caso, en la parte de host de la dirección de la subred anterior. Además nos sobra una red teniendo en cuenta el requerimiento.
