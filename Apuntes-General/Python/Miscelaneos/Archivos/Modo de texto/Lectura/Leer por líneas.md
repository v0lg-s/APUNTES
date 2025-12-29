# readline()

El método `readline()` permite manejar el archivo como un conjunto de líneas. Intenta leer línea por línea.

*Ej:*
```python
from os import strerror

try:
    character_counter = line_counter = 0
    stream = open('text.txt', 'rt')
    line = stream.readline()
    while line != '':
        line_counter += 1
        for char in line:
            print(char, end='')
            character_counter += 1
        line = stream.readline()
    stream.close()
    print("\n\nCaracteres en el archivo:", character_counter)
    print("Líneas en el archivo:     ", line_counter)
except IOError as e:
    print("Se produjo un error de E/S:", strerror(e.errno))
```

# readlines()

Cuando el método `readlines()` se invoca sin argumentos, intenta leer todo el contenido del archivo y devuelve una lista de cadenas.

Cuando se invoca con un argumento (Ese número es un hint: “lee aproximadamente hasta _N bytes_) el método intenta leer la cantidad de bytes especificados por el argumento con las siguientes reglas:

- Python **lee líneas completas** (no las parte).
- Lee una línea completa.
- Si ya llegó o se pasó del hint, para y devuelve lo que tiene.
- Si todavía no llega, lee otra línea completa, y así.

Ejemplo numérico (hint = 40):
- línea1 = 31 → acumulado 31 (aún < 40) → lee otra
- línea2 = 15 → acumulado 46 (ya > 40) → **se detiene** y devuelve 2 líneas

```python
stream = open("text.txt")
print(stream.readlines(20)) # ['Beautiful is better than ugly.\n']
print(stream.readlines(20)) # ['Explicit is better than implicit.\n']
print(stream.readlines(20)) # ['Simple is better than complex.\n']
print(stream.readlines(20)) # ['Complex is better than complicated.']
stream.close()
```

