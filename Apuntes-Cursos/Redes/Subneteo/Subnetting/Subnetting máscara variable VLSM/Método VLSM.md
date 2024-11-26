Con el método de máscara fija, vamos a poder dividir redes de un tamaño fijo. Con el método VLSM (Variable Length Subnet Mask) podemos dividir una red en subredes de distinto tamaño.

# Ejemplo VLSM
Dividir el segmento 192.168.0.0 /24 en 4 subredes con las siguientes especificaciones de Hosts en cada subred:

| Número de subred | Cantidad de Hosts |
| :--------------: | :---------------: |
|      LAN 1       |     28 hosts      |
|      LAN 2       |     50 hosts      |
|      LAN 3       |      2 hosts      |
|      LAN 4       |     10 hosts      |

**Solución**

**Paso #1:** Ordenar las subredes de mayor a menor número de hosts requeridos.

| Número de subred | Cantidad de Hosts |
| :--------------: | :---------------: |
|   $S_0$: LAN 2   |     50 hosts      |
|   $S_1$: LAN 1   |     28 hosts      |
|   $S_2$: LAN 4   |     10 hosts      |
|   $S_3$: LAN 3   |      2 hosts      |

**Paso #2:** Empezamos calculando la máscara de LAN 2, necesitamos una subred con capacidad para albergar 50 o más hosts. Por lo tanto, teniendo en cuenta la manera de calcular los hosts totales realizamos una desigualdad.
$$2^{n}-2=\text{Cantidad total de Hosts}$$
Con n=cantidad de ceros de la máscara de subred o bits para la parte de host.

$$2^{n}-2\geq50 $$
$$2^{n}\geq 52$$
Con las potencias de 2, tenemos que la potencia mayor más cercana: 
![[potencias.gif]]

n o el número de bits necesarios para la parte de hosts debe ser igual a 6.

$$2^{6}\geq 52$$
$$64\geq 52$$
**Paso #3:** Teniendo en cuenta lo anterior aplicamos el resultado de 6 bits para host sobre la máscara dada, es decir, sobre la máscara /24:

```
/24 = 11111111.11111111.1111111.00000000 
/24 = 255.255.255.0 
```

Necesitamos 6 bits en 0 de la máscara. Los tomamos de derecha a izquierda. 

/26 = 11111111.11111111.11111111.11<font color="red">000000</font> 
/26 = 255.255.255.192

**Paso #4:** Con los bits de host calculamos los saltos en este octeto. 
$$2^6=64$$
El último octeto ira de 64 en 64.

**Paso #5:** Se repite el proceso con las demás subredes. 
- Vamos con la **subred** $S_1$. Esta subred necesita 28 hosts:
$$2^{n}-2\geq 28 $$
$$2^{n}\geq30$$
$n=5$ para $S_1$
$$2^{5}\geq 30$$
$$32 \geq 30$$
Su máscara será:
/27 = 11111111.11111111.11111111.11100000
/27 = 255.255.255.224

- Vamos con la **subred $S_2$.** Esta subred necesita 10 hosts:
$$2^{n}-2\geq 10 $$
$$2^{n}\geq12$$
$n=4$  para $S_2$
$$2^{4}\geq 12$$
$$16 \geq 12$$
Su máscara será:
/28 = 11111111.11111111.11111111.11110000
/28 = 255.255.255.240

- Vamos con la **subred** $S_3$. Esta subred necesita 2 hosts:
$$2^{n}-2\geq 2 $$
$$2^{n}\geq4$$
$n=2$ para $S_3$
$$2^{2}\geq 4$$
$$4\geq 4$$
Su máscara será:
/30 = 11111111.11111111.11111111.11111100
/30 = 255.255.255.252

**Paso #6:** Construimos la tabla de rangos.

| # de Subred |  Dirección de Subred  | Dirección de Primer Host | Dirección Último Host |   Broadcast   |
| :---------: | :-------------------: | :----------------------: | :-------------------: | :-----------: |
|    $S_0$    |  192.168.0.0 **/26**  |       192.168.0.1        |     192.168.0.62      | 192.168.0.63  |
|    $S_1$    | 192.168.0.64 **/27**  |       192.168.0.65       |     192.168.0.94      | 192.168.0.95  |
|    $S_2$    | 192.168.0.96 **/28**  |       192.168.0.97       |     192.168.0.110     | 192.168.0.111 |
|    $S_3$    | 192.168.0.112 **/30** |      192.168.0.113       |     192.168.0.114     | 192.168.0.115 |
