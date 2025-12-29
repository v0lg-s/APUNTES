# Función system()
Tanto en Windows como en Unix la función `system()` está disponible.

Esta función nos permite ejecutar un comando que le es pasado como argumento.
La salida de la función será:
- En *Windows*, el valor devuelto por la shell después de ejecutar el comando dado.
- En *Unix*, devuelve el estado de salida del proceso. (0 si fue exitoso, 1 u otro de lo contrario)

```python
import os

retorno = os.system("mkdir my_directory")
print(retorno)
```

