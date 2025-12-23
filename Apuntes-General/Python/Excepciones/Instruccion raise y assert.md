*Raise* nos permite levantar nosotros mismos las excepciones.

```python
raise exception("Mensaje para mostrar")
```


---

*Assert* nos permite validar datos.

```python
assert expresion
```

- Si la expresión se evalúa como *True*, o un valor numérico *distinto de cero*, o una cadena *no vacía*, o cualquier otro valor *diferente de None*, no hará nada más.
- De lo contrario, automáticamente e inmediatamente se genera una excepción llamada *AssertionError* (en este caso, decimos que la afirmación ha fallado).

```python
import math

x = float(input("Ingresa un número: "))
assert x >= 0.0

x = math.sqrt(x)

print(x)
```

