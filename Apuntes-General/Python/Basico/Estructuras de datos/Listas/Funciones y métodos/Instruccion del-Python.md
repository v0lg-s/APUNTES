Se puede eliminar un elemento de una lista en cualquier momento, con la instrucción *del*. Se debe apuntar al elemento de la lista que se quiere eliminar:

```python
numbers = [10, 5, 7, 2, 1]
del numbers[1]
```

En este caso, se elimina el segundo elemento de la lista numbers.

Podemos especificar un rango de la lista para ser eliminado.

```python
my_list = [10, 8, 6, 4, 2]
del my_list[1:3]
print(my_list)
```

La lista ahora contiene: 10, 4, 2.