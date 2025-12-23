Dado que las cadenas son objetos iterables en python, algunas funciones que se pueden usar con las listas también se usan con las cadenas. Ese es el caso de *min()* y *max()*.

# Función min()

La función *min()* encuentra el elemento mínimo de la secuencia pasada como argumento. Con los caracteres lo hará basándose en su punto de código.

```python
# Demonstración de min() - Ejemplo 1:
print(min("aAbByYzZ")) # devuelve 'A' A = 65, a = 97


# Demonstración de min() - Ejemplos 2 y 3:
t = 'Los Caballeros Que Dicen "Ni!"' # devuelve espacio ' ' = 32
print('[' + min(t) + ']')

t = [0, 1, 2] # devuelve 0
print(min(t))
```

# Función max()

La función *max()* encuentra el elemento mínimo de la secuencia pasada como argumento. Con los caracteres lo hará basándose en su punto de código.

```python
# Demostración de max() - Ejemplo 1:
print(max("aAbByYzZ")) # devuelve 'z'


# Demostración de max() - Ejemplo 2 y 3:
t = 'Los Caballeros Que Dicen "Ni!"' 
print('[' + max(t) + ']') # imprime '[u]'

t = [0, 1, 2] # 2
print(max(t))
```