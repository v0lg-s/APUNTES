# Método .insert()
Añade un elemento en la posición indicada de una lista. Primer parámetro, es la posición, segundo parámetro es el elemento a añadir.

```python
lista = [1,2,3,5]
lista.insert(3,4)
```

El resultado será: `[1,2,3,4,5]`
# Método .remove()
Elimina la primera instancia de un objeto especificado en una lista. El único parámetro indica el elemento a eliminar.

```python
lista = [1,2,2,3,4,5]
lista.remove(2)
```

Eliminará el primer "2" que encuentre.
# Método .append()
Añade un elemento al final de la lista.

```python
lista = ["chevrolet", "mazda", "BMW"]

lista.append("toyota")
```

El resultado será: `["chevrolet", "mazda", "BMW", "toyota"]`
# Método .index()
Devuelve el índice de posición de un carácter especificado. (Devolverá la posición del primero en caso de que haya varios).

```python
username_list = ["bmoreno", "wjaffrey", "tshah", "sgilmore", "btang"]
username_index = username_list.index("tshah")
print(username_index)
```

