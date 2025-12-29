Usamos el método write para escribir un `bytearray` en un archivo binario.

```python
data = bytearray(10)

for i in range(len(data)):
    data[i] = 10 + i

try:
    bf = open('file.bin', 'wb')
    bf.write(data)
    bf.close()
except IOError as e:
    print("Se produjo un error de E/S:", strerror(e.errno))
```

- Devuelve la cantidad de bytes escritos correctamente.