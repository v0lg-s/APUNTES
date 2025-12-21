Con las listas también podemos crear matrices de dos dimensiones. Estas serán listas dentro de otra lista.

```python
tablero = []

for i in range(8):
	fila = ['EMPTY' for i in range(8)] # hace una lista de 8 elementos 'EMPTY'
	tablero.append(fila) # se agrega la lista 'fila' a la lista 'tablero'
```

así obtendremos:

```python
tablero: 
[
['EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY'],
['EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY'],
['EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY'],
['EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY'],
['EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY'],
['EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY'],
['EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY'],
['EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY', 'EMPTY']
]
```

Un tablero 8x8.

Colocar piezas:

```python
tablero[0][0] = 'TORRE'
tablero[0][7] = 'TORRE'
tablero[7][0] = 'TORRE'
tablero[7][7] = 'TORRE'
```
# Comprensión de arreglos
Así como las listas, podemos acortar la creación de los arreglos con la comprensión de listas.

```python
tablero = [['EMPTY' for _ in range(8)] for _ in range(8)]
```