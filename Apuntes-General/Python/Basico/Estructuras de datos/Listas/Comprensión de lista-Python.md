Es una sintaxis especial de Python para crear listas.

Forma tradicional de crear una lista:
```python
row = []

for i in range(8):
	row.append('PEON BLANCO')
```

Con comprensión de listas:

```python
row = ['PEON BLANCO' for i in range(8)]
```

# Ejemplos de uso

## Ejemplo 1
```python
cuadrados = [x ** 2 for x in range(10)]
```

Rellena la lista con cuadrados de diez números desde cero. (0, 1, 4, 9, 16, 25, 36, 49, 64, 81)

## Ejemplo 2

```python
impar = [x for x in range(1,10,2)]
```

Rellena la lista con números impares desde el 1 hasta el 10. (1, 3, 5, 7, 9)