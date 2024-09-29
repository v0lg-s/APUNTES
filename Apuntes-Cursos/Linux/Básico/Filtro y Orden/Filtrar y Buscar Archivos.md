# Buscar archivos

## Comando find
El comando *find* nos permite especificar una ruta en la cual buscar un archivo con los parámetros que escojamos.

Si lo ejecutamos así, hará una búsqueda recursiva desde el directorio en el que nos encontremos hacia adentro.

```bash
find .
```

### Filtros
- -type *Indicar el tipo de elemento que buscamos*
	- c → caracter
	- d → directorio
	- f → archivo
- -used **n** *Indicar que el archivo que se busca fue usado hace n días.*
	- mayor a n días: +n
	- menor a n días: -n
	- exactamente n días: n
- -name *Nombre del archivo que buscamos, podemos especificar que buscamos archivos que terminen con ciertos caracteres como jpg de la siguiente manera: \*.jpg *

### Acciones
- -delete *Encontrar el archivo especificado y eliminarlo(s)*

**REVISAR "man find" PARA MÁS INFO**

```bash
find ~/Descargas/ -name *.jpg
```

Encuentra todos los archivos en Descargas que tengan formato .jpg.

```bash
find ~/Descargas/ -name imagen*
```

Encuentra todos los archivos que incluyan la palabra "imagen" en su nombre.

### Dar formato a la salida
Es posible mediante el parámetro "*-printf*"  dar formato a la salida del comando find.
- La f tras print en el comando indica "format" y recibe como parámetro un formato.
- Otras variantes del comando son fprint cuya f al inicio indica "file" y recibe como parámetro un archivo.

```bash
find -printf "%f\t%M\n"
```

Esta linea de comando mostrará por linea de izquierda a derecha el nombre del archivo y los permisos de este.

![[findPrintf.png]]

Podemos encontrar mas información en el manual del comando escribiendo.

```bash
man find
```
## Comando grep
Podemos filtrar de la misma manera que con sort y podemos usar el operador [[Operadores#Operador "pipe "|pipe]] para redirigir salidas de comandos y filtrar.

Un ejemplo muy útil es para filtrar procesos en la lista de tareas activas. Usando el comando [[Procesos#Comando ps|ps -ef]]

```bash
ps -ef | grep brave
```

De esta manera obtendremos los procesos que está corriendo la aplicación brave.

![[grepCommand.png]]
