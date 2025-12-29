El modulo `os` tiene una función llamada `uname()` que devuelve un objeto que contiene los siguientes atributos:

- **systemname** - almacena el nombre del sistema operativo.
- **nodename** - almacena el nombre de la máquina en la red.
- **release** - almacena el release o actualización del sistema operativo.
- **version** - almacena la versión del sistema operativo.
- **machine** - almacena el identificador de hardware. (x86_64)

```python
import os
print(os.uname())
```


La función `uname()` funciona bien en sistemas Unix, en Windows la función `uname()` del modulo `platform` funciona.

**Atributo name**
Este atributo nos permite distinguir rápidamente entre sistemas operativos. Según la respuesta:

- `posix` - Se obtendrá este nombre si está usando Unix
- `nt` - Se obtendrá este nombre si está usando Windows.
- `java` - Se obtendrá este nombre si el código está escrito en Jython.

```python
import os
print(os.name)
```