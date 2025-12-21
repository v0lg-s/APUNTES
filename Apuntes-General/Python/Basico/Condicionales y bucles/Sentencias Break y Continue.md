Hay situaciones dentro de bucles que conviene:
- Pasar al siguiente ciclo del bucle sin completar la ejecución del actual.
- Cerrar la ejecución del bucle sin completar el resto de ciclos (o el ciclo actual incluso).

Para esto se usan las sentencias *Break* y *Continue*.

# break
Sale del bucle inmediatamente. El programa comienza a ejecutar la instrucción más cercana después del bucle.

```python
for i in range(1, 6):
    if i == 3:
        break
    print("Dentro del bucle.", i)
print("Fuera del bucle.")
```

# continue
Salta a la siguiente iteración, se considera la expresión de condición si se trata de un bucle while.

```python
for i in range(1, 6):
    if i == 3:
        continue
    print("Dentro del bucle.", i)
print("Fuera del bucle.")
```

