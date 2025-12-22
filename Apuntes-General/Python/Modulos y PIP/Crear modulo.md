Para crear un módulo e importarlo hagamos un ejemplo:

**Situación:**
Un script bajo nombre main.py se encuentra en la carpeta *progs*.
El módulo a importar llamado módulo.py está en una carpeta llamada *modules*.
Ambas carpetas, *modules* y *progs* están en una carpeta llamada *py*

`C:\Users\user\Desktop\Conocimiento\PYTHON\py\progs\main.py`
`C:\Users\user\Desktop\Conocimiento\PYTHON\py\modules\modulo.py`

**Entender como Python busca los módulos:**
Hay una variable especial (en realidad una lista) llamada[[Variables especiales -Python#Variable path | path]] que almacena todas las ubicaciones (carpetas o directorios) que se buscan para encontrar un módulo que ha sido solicitado por la instrucción import.

Python examina estas carpetas en el orden en que aparecen en la lista: si el módulo no se puede encontrar en ninguno de estos directorios, la importación falla.

De lo contrario, se tomará en cuenta la primera carpeta que contenga un módulo con el nombre deseado (si alguna de las carpetas restantes contiene un módulo con ese nombre, se ignorará).

Si vemos el valor de path desde el archivo `main.py` obtenemos:
```console
c:\Users\user\Desktop\Conocimiento\PYTHON\py\progs
C:\Python314\python314.zip
C:\Python314\DLLs
C:\Python314\Lib
C:\Python314
C:\Users\user\AppData\Roaming\Python\Python314\site-packages
C:\Python314\Lib\site-packages
```

Solución para poder importar el módulo, agregar la ubicación del módulo a la variable path.

```python
import sys

sys.path.append('c:\\Users\\user\\Desktop\\Conocimiento\\PYTHON\\py\\modules') # ruta absoluta. Solo funciona para el workspace actual.

import module
```

ó

```python
import sys
from pathlib import Path

modules_dir = Path(__file__).resolve().parent.parent / "modules" # Usa variables para definir el directorio padre y le agrega /modules.
sys.path.insert(0, str(modules_dir))

import module
```
