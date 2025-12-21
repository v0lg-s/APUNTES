Los operadores **Not, And y Or** miran la verdad del valor completo.
Un valor se evalúa así:
- **0** -> **False**
- **Cualquier otro número (1, 2, -3, 999, etc)** -> **True**

Se usa la doble negación para normalizar cualquier valor (Funciona con cualquier tipo de dato) a un booleano puro. 

```python
i = 45
j = not not i
# j = True

i = ""
j = not not i
# j = False
```

