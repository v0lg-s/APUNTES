Los módulos son archivos que contienen definiciones y sentencias de python reutilizables y útiles.

Cada modulo tiene entidades. Estas entidades pueden ser funciones, variables, constantes, clases y objetos, accediendo a un modulo se pueden usar cualquiera de las entidades que almacena.

# Importar módulos

Se usa la palabra clave `import` seguida del nombre del módulo.

```python
import math, sys # se importa el modulo math (con utilidades matematicas) y sys con utilidades para interactuar con el S.O
```

---
**Namespace:** Espacio en el que existen algunos nombres y los nombres no entran en conflicto entre sí. 

Por ejemplo, en el modulo `math` existe una entidad con el nombre `pi`. Si traigo sólo el módulo a mi *namespace*, puedo seguir usando el nombre `pi`. Sin embargo, si traigo a mi namespace la entidad con nombre `pi` habría conflicto y se solaparían.

---
## Llamada a las entidades del módulo fuera del namespace

Si solo se hace la importación con el nombre del módulo no se añaden las funciones (entidades) definidas en, `math` al *namespace*. Sólo añade el nombre del modulo. Usando el nombre del módulo se accede a las funciones u objetos.

```python
import math
print(math.sin(math.pi/2))

# modulo.entidad
```

## Agregar entidades al namespace

Se puede hacer la importación de entidades especificas del módulo.

```python
from math import sin, pi
print(sin(pi/2))
```

Se puede hacer la importación de TODAS las entidades del módulo.

```python
from math import *
```

Se pueden importar módulos o entidades específicas y darles un alias.

```python
import modulo as alias
from modulo import entity as alias

# ejemplo
from math import sin as seno
```