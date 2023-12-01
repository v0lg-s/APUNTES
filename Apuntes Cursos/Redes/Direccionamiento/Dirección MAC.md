# Que es la dirección MAC
¿Cómo saben las tramas a que dispositivo deben llegar?
Mediante la dirección MAC las interfaces de red ([[Trama de Ethernet#^8c195b|NIC]]) permiten o no el paso de las tramas, así:
- Cada interfaz de red o tarjeta de red tiene una única dirección MAC propia, si esta dirección no coincide con la dirección de destino en la trama de datos, la tarjeta de red rechazará esa trama.
- ==Dirección Física = Dirección MAC==

## Características
- Es una dirección de 48 bits.
- Tiene 12 dígitos hexadecimales, por lo tanto, 6 bytes.
- *Luce de la siguiente manera:*
	
		40-8D-5C-1C-5A-50 

 *Número OUI:* Los primeros 3 valores hacen referencia al número OUI (Identificador Único Organizacional), que identifica al fabricante de la NIC, que en este caso podría ser Intel. ==40-8D-5D==
 *Número Único:* Es el valor único asignado por el fabricante exclusivamente sobre el dispositivo. ==1C-5A-50==

## Funciones
Una de las **funciones de las direcciones MAC** está en el proceso de filtrado en redes inalámbricas. Para evitar que extraños accedan a una red, el enrutador está configurado para aceptar solo direcciones MAC específicas. De esta manera, si la dirección IP cambia, como por ejemplo en el caso de las direcciones IP dinámicas, la dirección MAC aún puede identificar el dispositivo.

El filtrado se puede utilizar para **rastrear a los usuarios de la red** y limitar su acceso. También puede tener otros usos, como **detectar cuándo un dispositivo robado se conecta a la red**. 

Por lo tanto, es importante que los propietarios de dispositivos ==no revelen sus direcciones MAC a nadie==, excepto al personal autorizado.