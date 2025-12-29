El método `write()` espera solo un argumento: una cadena que se transferirá a un archivo abierto.
No se agrega carácter de nueva línea automáticamente, hay que hacerlo manualmente.

*Ej:*

```python
from os import strerror

try:
    file = open('newtext.txt', 'w')
    for i in range(10):
        file.write("línea #" + str(i+1) + "\n")
    file.close()
except IOError as e:
    print("Se produjo un error de E/S: ", strerror(e.errno))
```

