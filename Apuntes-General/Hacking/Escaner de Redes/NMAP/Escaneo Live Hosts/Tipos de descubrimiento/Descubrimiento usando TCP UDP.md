En este tipo de descubrimiento existen tres subtipos de descubrimiento:

1. *Descubrimiento* **TCP SYN Ping**: Envía un paquete TCP con la flag *SYN* activa al puerto 80 por defecto, en este caso solo nos interesa saber si hay o no respuesta por parte del host, sin importar cual fue la respuesta. Si hay respuesta el host está activo.
2. *Descubrimiento* **TCP ACK Ping**: Envía un paquete TCP con la flag *ACK* activa al puerto 80 por defecto, se espera una respuesta con la flag *RST* activa. Si hay respuesta el host está activo.
3. *Descubrimiento* **UDP Ping**: Envía un paquete UDP a puertos UDP que posiblemente estén cerrados. Si el puerto UDP al que se envió el paquete está cerrado el host responde con un ICMP tipo 3 de lo contario no hay respuesta. Si hay respuesta el host está activo.

En los tres se pueden especificar los puertos en rangos, listas o específicos:

```bash
# **TCP SYN Ping**
sudo nmap -PS21 -sn MACHINE_IP/24 # al puerto 21
sudo nmap -PS80,443,8080 -sn MACHINE_IP/24 # a los puertos 80 443 y 8080

# **TCP ACK Ping** 
sudo nmap -PA21-25 -sn MACHINE_IP/24 # rango de puertos del 21 al 25
sudo nmap -PA80,443,8080 -sn MACHINE_IP/24

# **UDP Ping**
sudo nmap -PU80,443,8080 -sn MACHINE_IP/24

```
# Descubrimiento TCP SYN

```bash
# **TCP SYN Ping**
sudo nmap -PS -sn MACHINE_IP/24 
```

- Si se ejecuta como usuario root y en caso de que el o los puertos especificados estén abiertos no completa el [[Protocolo TCP#Three-Way Handshake|Three way handshake]], los usuarios sin permisos de root no tienen más opción que completarlo.
- Se usa la opción `-PS`.

# Descubrimiento TCP ACK

```bash
# **TCP ACK Ping** 
sudo nmap -PA -sn MACHINE_IP/24
```

- Requiere permisos privilegiados.
- Si el host está activo responde con *'RST'* ya que no se está llevando ninguna comunicación a cabo entre los dos dispositivos.
- Se usa la opción `-PA`.

# Descubrimiento UDP

```bash
# **TCP UDP Ping** 
sudo nmap -PU -sn MACHINE_IP/24
```

- Es probable que tome un poco más de tiempo ya que si existen puertos UDP abiertos no habrá una respuesta por parte del host.
- Se usa la opción `-PU`.