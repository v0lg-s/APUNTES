Estructura básica de un if en python:

```python
if condicion:
	# Instrucciones si verdadero
else:
	# instrucciones si falso 
```

Condiciones anidadas:

```python
if condicion1:
	# Instrucciones si verdadero
elif condicion2:
	# instrucciones si condicion1 falsa pero condicion2 verdadera 
elif condicion3:
	# instrucciones si condicion1 y condicion2 falsas pero condicion3 verdadera
else:
	# instrucciones si todas las condiciones son falsas 
```

# Otra forma de condicional

```python
expression_1 if condition else expression_2
```

En esta forma, el valor que proporciona es `expression_1` cuando la condición es `True` y `expression_2` cuando la condición es `False`.

```python
the_list = []

for x in range(10):
    the_list.append(1 if x % 2 == 0 else 0)

print(the_list)
```

