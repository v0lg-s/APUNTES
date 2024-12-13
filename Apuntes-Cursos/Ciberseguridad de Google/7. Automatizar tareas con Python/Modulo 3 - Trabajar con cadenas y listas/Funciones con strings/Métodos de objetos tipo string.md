# Método .upper()
Este método propio de objetos de tipo cadena, crea una copia de la cadena con todos los caracteres convertidos a mayúsculas.
# Método .lower()
Este método realiza lo contrario al anterior, crea una copia de una cadena con caracteres en mayúscula a una cadena en minúsculas.

```python
cadena = "ONIKUMA"
print(cadena.lower()) # Resultado: "onikuma".
```

# Método .index()
Devuelve el índice de posición de un carácter especificado. (Devolverá la posición del primero en caso de que haya varios).

```python
print("h32rb17r".index(r))
```

Lo anterior mostrará `3` que equivale al índice de la primer "r".

## Encontrar subcadenas
Una **Subcadena** es una secuencia continua de caracteres dentro de una Cadena. Por ejemplo, "llo" es una subcadena de "hello".

```python
tshah_index = "tsnow, tshah, bmoreno - updated".index("tshah")
print(tshah_index)
```

Devolverá el índice 7, que es donde comienza la subcadena *"tshah"*.