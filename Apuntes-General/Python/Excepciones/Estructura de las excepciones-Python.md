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


> [!NOTE] Algunas excepciones integradas abstractas
> - ArithmeticError,
> - BaseException
> - BaseException,
>- LookupError.
  
> [!NOTE] Algunas excepciones integradas concretas
>- AssertionError,
>- ImportError,
>- IndexError,
>- KeyboardInterrupt,
>- KeyError,
>- MemoryError,
>- OverflowError.








