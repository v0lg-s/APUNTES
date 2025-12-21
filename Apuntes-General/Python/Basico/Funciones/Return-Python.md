Hay dos variantes para usar return:

1. Return sin una expresión

```python
def happy_new_year(wishes = True):
    print("Tres...")
    print("Dos...")
    print("Uno...")
    if not wishes:
        return

    print("¡Feliz año nuevo!")
```

Provoca la terminación de la función.

2. Return con una expresión

```python
def boring_function():
    return 123

x = boring_function()

print("La función boring_function ha devuelto su resultado. Es:", x)
```

Evalúa el valor de la expresión y lo devuelve como resultado de la función.

**Nota:** Cuando una función no retorna cierto valor utilizando `return` se asume que devuelve `None`
