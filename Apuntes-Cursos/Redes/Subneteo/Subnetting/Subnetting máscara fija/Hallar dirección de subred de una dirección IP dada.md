A veces es necesario encontrar a qué subred pertenece una dirección IP dada, ya sea para conectar dispositivos que se puedan comunicar con el dispositivo que usa esa dirección IP o para fines de diagnostico. 

Si se nos da una dirección IP **172.33.43.5** con una máscara de subred **255.255.224.0 /19**, y se nos pide conectar otros dispositivos a la red de manera que se *puedan comunicar* con 172.33.43.5 (es decir, que estén en el mismo segmento de red) hay dos caminos que podemos tomar para hacerlo.

1. Hallar cada una de las subdivisiones de red usando la máscara de subred /19. Esto puede tomar más tiempo del necesario para determinar a qué subred pertenece la dirección dada. *"Método largo"*
2. Multiplicar la dirección IP dada con la máscara de subred en binario. También se puede ver como aplicar la operación lógica "AND" "&" entre estos dos números binarios. El resultado de esta operación será el segmento de red al que la dirección dada pertenece. *"Método corto"*

Vamos a ver con el ejemplo como se realizaría el procedimiento por el "método corto".

*Nota:* Para esto es útil tener en cuenta la siguiente tabla de conversión binaria a decimal.

![[binarios a decimales.jpeg]]

**Dirección IP:** 
172.33.43.5 -> 10101100.00100001.00101011.00000101
**Máscara de subred:** 
255.255.224.0 -> 11111111.11111111.11100000.00000000

Se realiza la operación AND bit a bit entre la máscara y la dirección.

$$\frac{10101100.00100001.00101011.00000101}{11111111.11111111.11100000.00000000}=10101100.00100001.00100000.00000000$$

Convertimos el resultado a decimal: 
10101100.00100001.00100000.00000000 -> 172.33.32.0

La dirección IP 172.33.43.5 pertenece a la subred:

**Subred**
- *Dirección de subred:* 172.33.32.0
- *Dirección de broadcast:* 172.33.63.255

Por lo que direcciones como: 
- 172.33.32.1
- 172.33.32.2
- 172.33.32.3
- 172.33.32.4
- 172.33.32.5

Se pueden asignar a hosts para que se puedan comunicar con la dirección dada.