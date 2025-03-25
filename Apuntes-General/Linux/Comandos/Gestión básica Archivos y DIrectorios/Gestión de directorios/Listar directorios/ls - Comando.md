## Comando ls
Este comando lista los directorios y archivos que se encuentran en la ruta en la que estamos actualmente.
- <font color ="#5883CF">ls → List</font>
![[comando-ls.png]]
### ls -a
Este argumento hace que se listen archivos y directorios que se encuentran ocultos, cuyo nombre empieza por un punto "."

```bash
ls -a
```

![[comando ls -a.png|450]]

### ls -l
Este argumento se usa para listar más información sobre los directorios y archivos.

```bash
ls -l
```

![[comando ls -l.png]]

- La primera columna de izq. a der. indica los permisos de cada directorio o archivo.
- La tercer columna indica el usuario al que le pertenece este directorio.
- La cuarta columna indica el grupo.
- La quinta columna es el tamaño del archivo o directorio.

### ls -al
Se pueden combinar los argumentos, en este caso, se listarán todos los directorios y ficheros incluyendo los ocultos y visibles junto a todos los detalles de fecha, tamaño, etc.

```bash
ls -al
```

## ls directorio
Podemos listar el contenido dentro de un directorio sin ingresar a él. Para eso se usa el comando:
```bash
ls nombre_directorio/
```