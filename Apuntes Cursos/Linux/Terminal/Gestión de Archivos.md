# Comando pwd
Este comando mostrará en pantalla la ruta del directorio en el que nos encontramos actualmente.
- <font color ="#5883CF">pwd → Print Working Directory</font>
![[pwd.png]]

# Comando ls
Este comando lista los directorios y archivos que se encuentran en la ruta en la que estamos actualmente.
- <font color ="#5883CF">ls → List</font>
![[comando-ls.png]]
## ls -a
Este argumento hace que se listen archivos y directorios que se encuentran ocultos, cuyo nombre empieza por un punto "."

```bash
ls -a
```

![[comando ls -a.png|450]]

## ls -l
Este argumento se usa para listar más información sobre los directorios y archivos.

```bash
ls -l
```

![[comando ls -l.png]]

- La primera columna de izq. a der. indica los permisos de cada directorio o archivo.
- La tercer columna indica el usuario al que le pertenece este directorio.
- La cuarta columna indica el grupo.
- La quinta columna es el tamaño del archivo o directorio.

## ls -al
Se pueden combinar los argumentos, en este caso, se listarán todos los directorios y ficheros incluyendo los ocultos y visibles junto a todos los detalles de fecha, tamaño, etc.

```bash
ls -al
```

## ls directorio
Podemos listar el contenido dentro de un directorio sin ingresar a él. Para eso se usa el comando:
```bash
ls nombre_directorio/
```
# Comando cd
Este comando nos permite movernos entre los directorios del sistema, recibe como argumento una ruta o el nombre de un directorio.
- cd → Change Directory

```bash
cd Desktop

# o

cd /home/volg/Desktop/
```

![[comando cd.png]]

Podemos volver al directorio anterior haciendo uso de:

```bash
cd ..
```

# Comando Touch
Este comando nos permite crear cualquier tipo de archivo especificando el nombre junto a la extensión del tipo de archivo. también permite cambiar la fecha de actualización de una archivo existente.

```bash
touch archivo.txt
```


# Comando cp
Este comando nos permite copiar un archivo desde un origen hacia un destino. Se puede especificar una ruta como destino y al final de la ruta el nuevo nombre de la copia del archivo
- cp → Copy
## Copiar archivos
```bash
cp archivo.txt archivo-copia.txt
```
- Lo anterior copia el archivo.txt en un archivo llamado archivo-copia.txt dentro del directorio en el que se está trabajando.
```bash
cp archivo.txt /home/volg/Downloads/archivo-copia.txt
```
- Lo anterior copia el archivo.txt en un archivo llamado archivo-copia.txt en el directorio Downloads.
## Copiar directorios
Para copiar un directorio junto a su contenido hacemos uso del argumento -r en el comando cp, de la siguiente manera:
```bash
cp -r directorio/ copia_directorio/
```


# Comando mv
El comando mv nos permite mover archivos y directorios, también nos permite hacer cambio de nombre.
mv → move
```bash
mv Downloads/ Downloads_mvd/
```

## mv -v
-v es un argumento que permite que se den detalles de lo que se está haciendo está disponible en varios comandos.
- v → verbose

# Comando file
El comando file permite ver más información acerca de un archivo en concreto, su tipo de archivo, resolución en caso de una imagen, tamaño, etc.

```bash
file archivo.jpg
```

![[comando file.png]]

# Comando rm
El comando rm permite eliminar archivos especificando su nombre o ruta.
- rm → remove

```bash
rm archivoNuevo.txt
```

# Comando cat
El comando cat nos permite mostrar el contenido de algunos archivos.
```bash
cat archivo.txt
```

