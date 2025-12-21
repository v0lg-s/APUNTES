Entre otros, existen los siguientes métodos:
## Obtener claves

```python
diccionario.keys()
```

Devuelve una lista con las claves.

---
## Obtener valores

```python
diccionario.values()
```

Devuelve una lista con los valores.

---
## Obtener todo el contenido
```python
diccionario.items()
```

Devuelve una lista de tuplas con los pares de clave-valor.
```python
[(clave, valor), (clave2, valor)]
```

---
## Eliminar elementos

```python
diccionario.pop(key)
```

Elimina la clave especificada y su valor. 

```python
diccionario.popitem()
```

Elimina el último elemento del diccionario.
## Agregar elementos

```python
dictionary.update({clave: valor })
```

Inserta un elemento al diccionario.