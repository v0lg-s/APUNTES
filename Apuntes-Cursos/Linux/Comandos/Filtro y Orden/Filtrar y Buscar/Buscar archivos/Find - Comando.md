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
- -iname *Lo mismo que name pero no distingue de mayúsculas o minúsculas.*
- -mtime *Encontrar archivos o directorios modificados por última vez dentro de un determinado periodo de tiempo*
	- introducir -mtime +1 indica todos los archivos o directorios modificados por última vez hace más de un día
	- Introducir -mtime -1 indica todos los archivos o directorios modificados por última vez hace menos de un día.
- -mmin *Lo mismo que mtime pero con minutos.*
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
