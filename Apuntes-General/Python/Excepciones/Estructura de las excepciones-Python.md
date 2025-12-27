Existen 63 excepciones integradas en Python 3, estas forman una jerarquía de árbol.

Hay excepciones más generales que otras (incluyen una gama de excepciones) y otras son completamente específicas. Cuanto más cerca de la raíz, mas abstracta es la excepción.

Por ejemplo:

![[fragmento_arbol_excepciones_python.png]]

`ZeroDivisionError` pertenece a la clase `ArithmeticError` que a su vez está dentro de `Exception` y por último este es un caso especial de la clase `BaseException`.

Si en el código a continuación se usa `ZeroDivisionError` solo capturará las excepciones de esa clase, sin embargo, si ponemos una clase más general como `ArithmeticError` capturará otras excepciones pertenecientes a esa clase.

```python
try:
    y = 1 / 0
except ZeroDivisionError:
    print("Uuupsss...")

try:
    y = 1 / 0
except ArithmeticError:
    print("Uuupsss...")
```

```python
def print_exception_tree(thisclass, nest = 0):
    if nest > 1:
        print("   |" * (nest - 1), end="")
    if nest > 0:
        print("   +---", end="")

    print(thisclass.__name__)

    for subclass in thisclass.__subclasses__():
        print_exception_tree(subclass, nest + 1)


print_exception_tree(BaseException)
```

Muestra el árbol de excepciones.




