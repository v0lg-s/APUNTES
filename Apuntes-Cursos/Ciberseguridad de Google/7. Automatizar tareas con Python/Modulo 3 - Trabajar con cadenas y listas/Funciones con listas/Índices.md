Al igual que las cadenas las listas tienen índices que indican su posición. Funciona de la misma manera. 0 es el primer índice.

## Notación entre corchetes
Igualmente en la notación entre corchetes, al especificar un índice en los corchetes obtendremos el objeto o elemento guardado en esa posición.

```python
username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
print(username_list[2]) # Devolverá "tshah"
```

- También se pueden indicar rangos de índices.

```python
username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
print(username_list[0:2])
```

Resultado: `['elarson', 'fgarcia']` 

Una lista a diferencia de un string, es modificable mediante los índices.

```python
username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
print("Before changing an element:", username_list)
username_list[1] = "bmoreno"
print("After changing an element:", username_list)
```

El código anterior actualiza el elemento en el índice 1 `"fgarcia"` por `"bmoreno"`
