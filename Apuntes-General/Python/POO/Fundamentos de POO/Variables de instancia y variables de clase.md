# Variables de instancia
Cada objeto lleva su propio conjunto de propiedades, no interfieren entre sí y puede diferir del conjunto de otros objetos
Estas propiedades de cada uno de los objetos de una clase son llamadas variables de instancia.

## Variable \_\_dict__
Cada objeto está dotado de unas propiedades y métodos predefinidos, uno de ellos es la variable \_\_dict__.
Esta variable almacena un diccionario con los nombres y valores de todas las propiedades del objeto o una clase.

```python
class ExampleClass:
    def __init__(self, val = 1):
        self.first = val

    def set_second(self, val):
        self.second = val


example_object_1 = ExampleClass()
example_object_2 = ExampleClass(2)

example_object_2.set_second(3)

example_object_3 = ExampleClass(4)
example_object_3.third = 5

print(example_object_1.__dict__)
print(example_object_2.__dict__)
print(example_object_3.__dict__)

# Atributos y métodos de la clase
print(ExampleClass.__dict__)
```

```python
{'_ExampleClass__first': 1}
{'_ExampleClass__first': 2, '_ExampleClass__second': 3}
{'_ExampleClass__first': 4, '__third': 5}
```

**Nota:** Aunque la propiedad *\_\_third__* no está definida dentro de la definición de clase, sobre la marcha se enriqueció el objeto *example_object_3* con esta propiedad. Esto es posible.

# Variables de clase
Las variables de clase son propiedades compartidas por todos los objetos y se almacena fuera de cualquier objeto. Son usadas internamente por la clase.

**Nota**: no existe una variable de instancia si no hay ningún objeto de la clase; solo existe una variable de clase en una copia, incluso si no hay objetos en la clase.

```python
class ExampleClass:
    counter = 0
    def __init__(self, val = 1):
        self.__first = val
        ExampleClass.counter += 1


example_object_1 = ExampleClass()
example_object_2 = ExampleClass(2)
example_object_3 = ExampleClass(4)

print(example_object_1.__dict__, example_object_1.counter)
print(example_object_2.__dict__, example_object_2.counter)
print(example_object_3.__dict__, example_object_3.counter)
```

```python
{'_ExampleClass__first': 1} 3

{'_ExampleClass__first': 2} 3

{'_ExampleClass__first': 4} 3
```

