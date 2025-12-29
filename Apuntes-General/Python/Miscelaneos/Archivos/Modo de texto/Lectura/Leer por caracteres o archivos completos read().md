# read() - Leer caracteres o archivos completos

Si el método `read()` se aplica a un archivo de texto, es capaz de:

- Leer un número determinado de caracteres del archivo y devolverlos como cadena.
- Leer todo el contenido de un archivo y devolverlo como una cadena.
- Cuando se acaban los caracteres devuelve una cadena vacía.

Si el método es invocado con un argumento, leerá la cantidad de caracteres (bytes) especificados en el argumento.

*Ej:*
Carácter por carácter. Se invoca con `1` como argumento, leerá byte por byte. (Lo que ocupa un carácter)
```python
from os import strerror

try:
    counter = 0
    stream = open('text.txt', "rt")
    char = stream.read(1)
    while char != '':
        print(char, end='')
        counter += 1
        char = stream.read(1)
    stream.close()
    print("\n\nCaracteres en el archivo:", counter)
except IOError as e:
    print("Se produjo un error de E/S: ", strerror(e.errno))
```

Todo el archivo de una (sin argumentos)
```python
from os import strerror

try:
    counter = 0
    stream = open('text.txt', "rt")
    content = stream.read()
    for char in content:
        print(char, end='')
        counter += 1
    stream.close()
    print("\n\nCaracteres en el archivo:", counter)
except IOError as e:
    print("Se produjo un error de E/S: ", strerr(e.errno))
```

**Nota:** el leer un archivo muy grande (en terabytes) usando este método puede dañar el sistema operativo.