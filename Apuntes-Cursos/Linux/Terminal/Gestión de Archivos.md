# Mostrar directorio actual
## Comando pwd
Este comando mostrará en pantalla la ruta del directorio en el que nos encontramos actualmente.
- <font color ="#5883CF">pwd → Print Working Directory</font>
![[pwd.png]]

# Moverse entre el sistema
## Comando cd
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

# Crear archivos 
## Comando Touch
Este comando nos permite crear cualquier tipo de archivo especificando el nombre junto a la extensión del tipo de archivo. También permite cambiar la fecha de actualización de una archivo existente.

```bash
touch archivo.txt
```

# Copiar archivos 
## Comando cp
Este comando nos permite copiar un archivo desde un origen hacia un destino. Se puede especificar una ruta como destino y al final de la ruta el nuevo nombre de la copia del archivo
- cp → Copy
### cp archivos
```bash
cp archivo.txt archivo-copia.txt
```
- Lo anterior copia el archivo.txt en un archivo llamado archivo-copia.txt dentro del directorio en el que se está trabajando.
```bash
cp archivo.txt /home/volg/Downloads/archivo-copia.txt
```
- Lo anterior copia el archivo.txt en un archivo llamado archivo-copia.txt en el directorio Downloads.
### cp directorios
Para copiar un directorio junto a su contenido hacemos uso del argumento -r en el comando cp, de la siguiente manera:
```bash
cp -r directorio/ copia_directorio/
```


# Mover Archivos
## Comando mv
El comando mv nos permite mover archivos y directorios, también nos permite hacer cambio de nombre.
mv → move
```bash
mv Downloads/ Downloads_mvd/
```

### mv -v
-v es un argumento que permite que se den detalles de lo que se está haciendo está disponible en varios comandos.
- v → verbose

# Listar información de archivos

## Comando file
El comando file permite ver más información acerca de un archivo en concreto, su tipo de archivo, resolución en caso de una imagen, tamaño, etc.

```bash
file archivo.jpg
```

![[comando file.png]]

# Eliminar Archivos 
## Comando rm
El comando rm permite eliminar archivos especificando su nombre o ruta.
- rm → remove

```bash
rm archivoNuevo.txt
```

# Mostrar contenido de archivos
## Comando cat
El comando cat nos permite mostrar el contenido de algunos archivos.
```bash
cat archivo.txt
```



