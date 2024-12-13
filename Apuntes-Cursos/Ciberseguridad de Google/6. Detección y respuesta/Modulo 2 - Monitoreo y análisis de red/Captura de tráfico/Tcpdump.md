El analizador de paquetes tcpdump es un analizador de red de línea de comandos CLI. 
- El tráfico capturado por tcpdump es almacenado en un archivo llamado *p-cap* 

# Comando y opciones
```bash
sudo tcpdump [-i interface] [option(s)] [expression(s)]
```

- Para especificar la interfaz de red para capturar el tráfico se usa `-i`. `-i any` Hará uso de todas las interfaces de red disponibles para olfatear.

## Opciones
También son conocidas como flags o banderas. Hay mas de cincuenta opciones en tcpdump.
- Las opciones distinguen entre mayúsculas y minúsculas.
**Ejemplos:**

- **-w:** Puede escribir o guardar los paquetes de red olfateados en un archivo de captura de paquetes en lugar de simplemente imprimirlos en el terminal.

```bash
sudo tcpdump -i any -w packetcapture.pcap 
```

- **-r:** Puede leer un archivo de captura de paquetes, especificando el nombre como parametro.

```bash
sudo tcpdump -i any -r packetcapture.pcap
```

- **-v:** Verbose. Permite controlar la cantidad de información mostrada. Hay tres niveles de detalle que aumentan cuando se aumentan la cantidad de *"v's"* en la opción.

```bash
sudo tcpdump -i any -r packetcapture.pcap -vv
```

- **-c:** Significa recuento. Permite controlar cuántos paquetes capturará tcpdump. Si elige `-c 1` solo se imprimirá un paquete.

```bash
sudo tcpdump -i any -c 3
```

- **-n:** Desactiva la resolución de nombres de dominio por defecto de tcpdump. Es útil para ser sigilosos durante una investigación en un sistema atacante.
- **-nn:** Desactiva la resolución de nombres de dominio y de puertos.

```bash
sudo tcpdump -r packetcapture.pcap -vn
```

**Nota:** Se puede combinar una opción con otra de la manera `-vn` para `-v` y `-n` siempre y cuando estas no acepten parámetros para funcionar.

## Expresiones
Mediante estas expresiones podemos filtrar las búsquedas y capturas. Por ejemplo, se puede filtrar la búsqueda por protocolo.

```bash
sudo tcpdump -r packetcapture.pcap -n 'ip and (port 80 or port 443)'
```

Los paréntesis indican a tcpdump que priorice la ejecución de los filtros encerrados entre los paréntesis antes de filtrar para IPv4.