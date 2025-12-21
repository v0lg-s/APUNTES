Una función puede tener tantos parámetros como se desee.

```python
def message(number):
	print("Ingresa el número: ", number)
```

# Parámetros posicionales

Toman el valor según la posición del parámetro en la definición de la función.

```python
def introduction(first_name, last_name):
	print("Mi nombre es ", first_name, last_name)

# llamado a la función
introduction("James", "Bond")
# Salida: Mi nombres es James Bond
introduction("Bond", "James")
# Salida: Mi nombre es Bond James
```

# Anotaciones a los argumentos

Anotaciones de tipo que nos permiten restringir los argumentos y retornos de una función a un tipo especifico.

```python
def filtrar_pares(salida: 'list' = []) -> 'list': 
	return [i for i in salida if i%2 == 0] 

print(filtrar_pares([1, 2, 3, 4, 5, 6])) # Salida: [2, 4, 6]
```

En este ejemplo, además, se da un valor por defecto.
# Valores predeterminados en argumentos

Se pueden definir valores por defecto para los parámetros de una función. Por lo que al hacer el llamado ya no es necesario darle un valor a ese parámetro.

```python
def introduction(first_name, last_name="Rodriguez"):
     print("Hola, mi nombre es ", first_name, last_name)

# Llamado normal
introduction("Jorge", "Perez") # Salida: Hola, mi nombre es Jorge Perez

# Llamado solo con un parámetro
introduction("Andrés") # Salida: Hola, mi nombre es Andrés Rodriguez
```

