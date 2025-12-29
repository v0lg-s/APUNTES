Bytearray es una clase especializada que puede contener datos amorfos (datos sin forma especifica, solo una serie de bytes). Es un arreglo que contiene bytes amorfos.

Se puede crear de diferentes maneras, una de ellas es usando su constructor.

```python
data = bytearray(10)
```

Crea un objeto de `bytearray` capaz de almacenar diez bytes, el constructor llena el arreglo con ceros.

- Son mutables
- Son susceptibles a la función [[Funcion len-Python |len()]].
- Son indexables (manejan índices)

*Limitaciones:* 
- No se debe establecer ningún elemento con un valor no entero.
- No está permitido asignar un valor fuera del rango de 0 a 255