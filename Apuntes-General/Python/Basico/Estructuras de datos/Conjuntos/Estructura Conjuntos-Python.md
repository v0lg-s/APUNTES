Es una colección de elementos, esta colección tiene las siguientes características:

**Características**
- **No ordenados:** No maneja índices, por lo que la posición de cada elemento dentro de la estructura no importa.
- **Heterogéneas:** Almacenan distintos tipos de datos.
-  **Mutables:** Se pueden modificar. (modificando, eliminando o añadiendo elementos)
- **Sin repetición:** No hay elementos iguales. 

*Sintaxis*
Se utiliza el constructor de conjuntos `set`.

```python
#conjuntos
conjunto = set([5,3,2,1])
```

*Si se le pasa un string, set lo interpretará como una lista de caracteres y el conjunto se verá así:*

```python
conjunto = set("Hola, que")
print(conjunto)
```

La salida es: `{'h', 'o', 'l', 'a', ' ', 'q', 'u', 'e'}`

