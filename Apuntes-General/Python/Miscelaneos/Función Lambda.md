La función *Lambda* sirve para simplificar el código, hacerlo más claro y fácil de entender.

Una función *Lambda* es una función anónima o sin nombre, se declara de la siguiente manera:

```python
lambda parametro1, ..., parametroN: expresión
```

*Ejemplo:*

```python
two = lambda: 2
sqr = lambda x: x * x
pwr = lambda x, y: x ** y

for a in range(-2, 3):
    print(sqr(a), end=" ")
    print(pwr(a, two()))
```

Si es una función que queremos usar una vez y no necesitamos almacenarla en una variable se hace:
```python
(lambda a,b: a + b)(2, 4)
```

# Ejemplos de utilidad

## Función filter()
La función *filter* aplica la función en su primer argumento a los elementos del iterable en el segundo argumento. Los elementos que devuelven `True` desde la función pasan el filtro, el resto son rechazados.

```python
from random import seed, randint

seed()
data = [randint(-10,10) for x in range(5)]
filtered = list(filter(lambda x: x > 0 and x % 2 == 0, data))

print(data)
print(filtered)
```

Aquí *lambda* se usa para evaluar una expresión a un conjunto de datos, como una función, pero sin ser almacenada.

## Función map()
La función *map* toma como primer argumento una función y uno o más iterables según lo que reciba la función como argumento. Map aplica la función pasada como argumento a cada uno de los elementos de los iterables.

```python
my_list = [1, 2, 3]
foo = tuple(map(lambda x: x**x, my_list))
print(foo)
```