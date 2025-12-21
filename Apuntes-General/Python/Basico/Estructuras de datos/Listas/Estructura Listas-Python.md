Es un tipo de dato en python que permite almacenar una secuencia de datos ordenados, sin importar su tipo, es decir, una lista puede almacenar desde datos de tipo **`int`** **`float`** incluso otras listas.

**Características:**
- **Ordenadas:** La posición dentro de la estructura importa. (Maneja indices)
- **Heterogéneas:** Almacenan distintos tipos de datos.
- **Mutables:** Se pueden modificar durante la ejecución. (modificando, eliminando o añadiendo elementos)

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

- Se pueden poner indices negativos para recuperar los datos en sentido contrario (del último al primero).

```python
numbers = [111, 7, 2, 1]
print(numbers[-1]) # devuelve el último de la lista: 1
```

# Rebanadas

Un elemento de la sintaxis de Python que permite hacer una copia nueva de una lista, o partes de una lista. Esto es llamado *rebanada* de una lista.

```python
list_1 = [1]
list_2 = list_1[]
list_1[0] = 2
print(list_2)
```

Si comprobamos lo anterior, veremos que *list_2* y *list_1* apuntan a la misma dirección de memoria, es decir, la misma lista.

Si queremos hacer una copia de la lista 1 y guardarla en la lista 2 como una nueva lista, tendremos que hacer uso de las rebanadas.

```python
list_1 = [1]
list_2 = list_1[:]
list_1[0] = 2
print(list_2)
```

Con tan solo poner ':' le damos a list_2 una nueva lista con los mismos valores de list_1.
