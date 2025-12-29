# Método read()

El método *read()* devuelve un objeto `bytes` del tamaño especificado nuevo en cada lectura.

```python
with open("file.bin", "rb") as f:
	chunk = bytearray(f.read(4096))
```
# Método readinto()
El método *readinto()* no crea un nuevo objeto del arreglo de bytes, llena uno ya creado previamente.

- Puede ser más eficiente en lectura repetida.
- El método devuelve el número de bytes leídos con éxito.

```python
buf = bytearray(4096)
with open("file.bin", "rb") as f:
    while True:
        n = f.readinto(buf)     # n = bytes leídos
        if n == 0:
            break
        procesar(buf[:n])
```

