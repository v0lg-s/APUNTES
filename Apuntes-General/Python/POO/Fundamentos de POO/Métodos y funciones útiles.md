# Funciones
## Verificar existencia de un atributo

En Python existe la función `hasattr()` que recibe dos argumentos:
1. *Clase u objeto que se verifica*
2. *Nombre del atributo cuya existencia se debe verificar*

La función devuelve `True` o `False` de acuerdo a si existe o no el atributo.

```python
class ExampleClass:
    attr = 1


print(hasattr(ExampleClass, 'attr')) # True
print(hasattr(ExampleClass, 'prop')) # False
```

## Obtener y definir el valor de un atributo

En Python se usa la función `getattr()` para obtener el valor de una propiedad/atributo de un objeto. Recibe los mismos argumentos que `hasattr()`.
1. *Clase u objeto que se verifica*
2. *Nombre del atributo cuyo valor queremos conocer.*

En Python se usa la función `setattr()` para obtener el valor de una propiedad/atributo de un objeto. Recibe los mismos argumentos que `getattr()` más un tercero.
1. *Clase u objeto que se verifica*
2. *Nombre del atributo cuyo valor queremos definir.*
3. *Valor que queremos asignarle a dicho atributo*

```python
def incIntsI(obj):
    for name in obj.__dict__.keys():
        if name.startswith('i'):
            val = getattr(obj, name)
            if isinstance(val, int):
                setattr(obj, name, val + 1)
```

## Saber si es una clase hija

La función `issubclass()` nos permite conocer si una función dada es subclase de otra función pasada como argumento.

```python
issubclass(ClassOne, ClassTwo)
```

## Saber si es una instancia

La función `isinstance()` devuelve `True` si el objeto pasado como argumento es instancia de la clase pasada como argumento.

```python
isinstance(objectName, ClassName)
```
# Métodos

## Método \_\_str__
Todas las clases tienen un método llamado `__str__` que devuelve información de un objeto especifico. Es responsable de convertir el contenido de un objeto en una cadena (más o menos) legible.

```python
class Star:
    def __init__(self, name, galaxy):
        self.name = name
        self.galaxy = galaxy


sun = Star("Sol", "Vía Láctea")
print(sun)
```

```python
<__main__.Star object at 0x7f1074cc7c50>
```

Podemos anular el método para acomodarlo a nuestro gusto.

```python
class Star:
    def __init__(self, name, galaxy):
        self.name = name
        self.galaxy = galaxy

    def __str__(self):
        return self.name + ' en ' + self.galaxy


sun = Star("Sol", "Vía Láctea")
print(sun)
```

```python
Sol en Vía Láctea
```

