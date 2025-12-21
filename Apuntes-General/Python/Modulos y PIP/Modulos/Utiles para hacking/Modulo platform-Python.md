Permite acceder a los datos de la plataforma subyacente (sistema en el que se ejecuta el código).

**Funciones**

1. **platform**
```python
from platform import platform
platform(aliased = False, terse = True)
```

- *aliased:* Si se establece en True hace que la función presente los nombres de capa subyacentes alternativos en lugar de los comunes.
- *terse:* Si se establece en True hace que la función presente de una forma más breve el resultado. (Si es posible)

---
2. **machine()**

```python
from platform import machine
print(machine())
```

- Nombre genérico del procesador que ejecuta el sistema operativo.

--- 

3. **processor()**

```python
from platform import processor
print(processor())
```

- Devuelve una cadena con el nombre real del procesador (si lo fuese posible).

---
4. **system()**

```python
from platform import system
print(system())
```

- Devuelve una cadena con el nombre del sistema operativo.

--- 
5. **version()**

```python
from platform import version
print(version())
```

- Versión del sistema operativo como cadena.

--- 
6. **python_implementation() & python_version_tuple()**

```python
from platform import python_implementation, python_version_tuple

print(python_implementation())

for atr in python_version_tuple():
    print(atr)
```

- `python_implementation()` → devuelve una cadena que denota la implementación de Python.
- `python_version_tuple()` → devuelve una tupla de tres elementos la cual contiene:
    - La parte **mayor** de la versión de Python.
    - La parte **menor**.
    - El número del nivel de **parche**.

