Los elementos de una cadena tienen asignado un **índice**, que es un número que indica su posición en la cadena.

Los índices comienzan en 0, es decir, el primer índice o posición de izquierda a derecha será 0. 

**Ejemplo:**
La cadena "hello" tiene índices del 0 a 4:

| Carácter | Índice |
| :------: | :----: |
|    h     |   0    |
|    e     |   1    |
|    l     |   2    |
|    l     |   3    |
|    o     |   4    |
Se pueden usar índices negativos:

| Carácter | Índice |
| :------: | :----: |
|    h     |   -5   |
|    e     |   -4   |
|    l     |   -3   |
|    l     |   -2   |
|    o     |   -1   |
En este caso, la enumeración de índices se basa en la posición respecto al último carácter de la cadena. Cuyo índice siempre será -1.

## Notación entre corchetes para índices.
La notación entre corchetes nos permite extraer una parte de la cadena.

```python
string= "hello"
string[0] # Esto devolverá "h".
```

- Se pueden indicar rangos para extraer más de un carácter. En este caso, se retornarán los valores en el rango de índices del 0 al 2, es decir, uno menos al número especificado en los corchetes.

```python
string = "Prueba"
string[0:3] # Esto devolverá "Pru"
```

