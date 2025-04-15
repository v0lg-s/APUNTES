Es una estructura de datos que nos permite relacionar dos elementos, 'clave' y 'valor'.
- La *clave* o *key* sirve para identificar y buscar el elemento con el que está relacionado, es decir, el *valor* o *value*.

**Estructura**
La clave y el valor tienen una estructura específica. {clave:valor}
**Características**
- Los diccionarios no tienen orden.
- Es heterogéneo.
- Las claves son inmutables. (Si se repite dentro del diccionario, tomará el valor de la última aparición)
- Los valores son mutables.
- Es mutable.

*Sintaxis*
```python
#diccionario
dictionary = {"clave1": 1, "clave2": 2, 3: "tres"}
```

Para ver el contenido del diccionario se usan las claves, por ejemplo, si quiero ver el valor de la clave "clave1", usaría:

```python
print(dictionary["clave1"]) # Resultado: Numero 1 en pantalla
print(dictionary[3]) # Resultado: Cadena "tres" en pantalla
```

**Ejemplos:**

Función Dict para crear diccionarios. Recibe una secuencia con los pares de elementos (listas o tuplas)

Diccionario con lista de tuplas.

```python
dict_list_tuples = dict([(1,"Uno"),(2,"Dos"),(3,"Tres")])
print(dict_list_tuples) # Resultado: {1: 'Uno', 2: 'Dos', 3: 'Tres'}
```

Diccionario con strings

```python
dict_list_tuples = dict(Uno = 1, Dos = 2, Tres = 3)
print(dict_list_tuples) # Resultado: {'Uno': 1, 'Dos': 2, 'Tres': 3}
```

