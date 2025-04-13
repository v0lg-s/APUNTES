Es un tipo de dato en python que permite almacenar una secuencia de datos ordenados, sin importar su tipo, es decir, una lista puede almacenar desde datos de tipo **`int`** **`float`** incluso otras listas.

**Características:**
- **Ordenadas:** La posición dentro de la estructura importa. (Maneja indices)
- **Heterogéneas:** Almacenan distintos tipos de datos.
- **Mutables:** Se pueden modificar. (modificando, eliminando o añadiendo elementos)

*Sintaxis:*

```python
#Listas
lista = [29, True, "Cadena de texto", 3.1416, [1,2,3]]
```

- Los elementos van dentro de corchetes, cada uno separado por una coma.

**Indices**
Para acceder a cada uno de sus elementos podemos usar la posición de cada elemento. Dentro de corchetes

```python
print(lista[0]) #para el primer elemento
```

- Se puede solicitar un rango de elementos de una lista.

```python
print(lista[1:3]) #Devuelve una lista desde el elemento con indice 1 hasta el 2. (1 menos que el último número del rango)
```

