Es la forma en la que se organizan los datos en el transmisor para ser enviados por el medio físico y entendidos por el receptor. Solo se habla de trama ethernet cuando es una trama que viaja en la red local o LAN.
- **Generalidades:**  ^8c195b
	- Las tramas de datos son trozos con un tamaño de 1500 bytes.
	- Los dispositivos de una red envían y reciben datos de esta manera, mediante tramas.
	- Las tramas se ==crean y destruyen en las interfaces de red o tarjetas de red (NIC) Network Interface Card== de cada dispositivo. 
- **La trama se compone de la siguiente manera:** 

==El número arriba de cada campo indica la cantidad de bytes que ocupa el campo.\*==
![[trama-ethernet.png|650]]

1. *Preámbulo:* Se compone de un patrón de 1's y 0's (intercalados) cuyo objetivo es darle una señal al hardware del receptor que indica que se está por recibir información para que ambas interfaces (NIC) se sincronicen.
2. *SFD(Start Frame Delimiter):* Su función es la de sincronizar las porciones de recepción de trama de todas las estaciones de la red. Finaliza con dos bits "1" consecutivos para indicar el final de su espacio y el comienzo de la dirección MAC de destino.
3. *Dirección de Destino:* Indica cual de los equipos en la LAN es el receptor de la trama. Pueden ser direcciones MAC o IP.
4. *Dirección de Origen:* Indica desde que equipo se envían dichos datos, es una dirección MAC o IP.
5. *Longitud/Tipo:* Puede contener tanto la longitud de los datos que se envían como el "tipo", este último indica el protocolo de capa superior que recibe los datos una vez se completa el procesamiento.
6. *Datos:* Datos encapsulados que están siendo enviados. Si no se completa el mínimo se rellena de algunos bytes de relleno. Máximo de 1500 bytes (MTU)
7. *FCS (Frame Check Sequence):* Es un código que se crea en la maquina transmisora a partir de todos los otros campos de la trama, posteriormente, la maquina receptora vuelve a calcularlo con los datos recibidos y lo compara con el que se recibe, si coincide, indica que los datos han llegado íntegramente, de otro modo, indica que no ha sido así.





