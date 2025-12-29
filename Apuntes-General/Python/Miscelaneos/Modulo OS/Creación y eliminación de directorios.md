# Creación
## Crear un directorio en Python
A modo de ejemplo, usemos el comando `mkdir` que crea directorios tanto en sistemas Unix como Windows.

```python
import os

os.mkdir("directorio_nuevo")
print(os.listdir()) # devuelve una lista con los nombres de archivo y directorios que se encuentran en la ruta pasada como argumento.
```

## Crear directorios recursivamente
La función `makedirs()` permite la creación recursiva de directorios, se van a crear todos los directorios pasados como ruta.

```python
import os
os.makedirs("my_directory/my_second_directory")
os.chdir("my_directory")
pritn(os.listdir()) # va a mostrar ['my_second_directory']
```

# Eliminar

## Eliminar un directorio
Se usa el método `rmdir()`.

```python
import os

os.mkdir("my_first_directory")
print(os.listdir())
os.rmdir("my_first_directory")

print(os.listdir())
```

## Eliminar un directorio y sus subdirectorios
Se usa el método `removedirs()`, que requiere como argumento una ruta con todos los directorios a eliminar.

```python
import os

os.makedirs("my_first_directory/my_second_directory")
os.removedirs("my_first_directory/my_second_directory")

print(os.listdir())
```

Si no están vacíos se genera una excepción.