# Opciones para tipos de escaneos de puertos

**Tipos de escaneos comunes**
- `-sS` Opción para ejecutar un escaneo *'TCP SYN Scan'*. [[TCP SYN Scan]]
- `-sU` Opción para ejecutar un escaneo *'UDP Scan'*. [[UDP Scan]]
- `-sT` Opción para ejecutar un escaneo *'TCP Connect Scan'*. [[TCP Connect Scan]]

**Otros tipos**
- `-sN` Opción para ejecutar un escaneo *'TCP NULL Scan'*. [[NULL, FIN Xmas Scan]]
- `-sF` Opción para ejecutar un escaneo *'TCP FIN Scan'*. [[NULL, FIN Xmas Scan]]
-  `-sX` Opción para ejecutar un escaneo *'TCP Xmas Scan'*. [[NULL, FIN Xmas Scan]]

# Agresividad y Output
Para *guardar la salida del escaneo en archivos* se pueden usar varias opciones:
- `-oA 'nombre de archivo'` Guardar los resultados en los *tres grandes formatos .nmap .xml .gnmap.*
- `-oN 'nombre de archivo'`  Guardar los resultados en *formato normal.*

Para ser *agresivos* se puede usar la opción `-A`.
- `-A` Activa: la detección de servicios, sistemas operativos, trace-route y escaneo con scripts comunes.

Cambiar *velocidad del escaneo*:
- `-T1-5` Cambia la velocidad del escaneo por niveles del 1 al 5. Un nivel más alto es más ruidoso y puede incurrir en errores.
# Detalles
Para que el escaneo de NMAP sea más detallado en consola se utiliza la opción `-v` entre más 'v' se utilicen más detallada va a ser la ejecución del escaneo. De 1-3 niveles de detalle.

```bash
nmap -v
nmap -vv
nmap -vvv
```

# Sistema Operativo y Versiones

- `-O` Opción para detectar qué sistema operativo usa el objetivo.
- `-sV` Opción para detectar las versiones de los servicios corriendo en el objetivo.

# Rangos de puertos

- `-p` Se usa esta opción para especificar puertos o rangos de puertos a escanear.

```bash
nmap -p 80 //escanear puerto 80
nmap -p 1000-1500 //escanear puertos del 1000 al 1500
nmap -p- //escanear todos los puertos. -p0- para escanear desde el 0
```

# Scripts
Para ejecutar scripts con nmap se usa la opción `--script`.

```bash
nmap --script='nombre del script'
```