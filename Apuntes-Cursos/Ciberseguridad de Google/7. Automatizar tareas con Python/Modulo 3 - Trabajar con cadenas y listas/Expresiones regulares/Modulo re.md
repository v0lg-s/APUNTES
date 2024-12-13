Es una secuencia de caracteres que indican un patrón. Se puede usar para buscar direcciones IP, correos electrónicos o ID de dispositivos.

Si queremos trabajar con expresiones regulares en Python es necesario importar el modulo ``re``.

```python
import re
```

# Función modulo re findall()
La función `findall()` del módulo `re` tomará como parámetros dos cosas:
1. La expresión regular que indicará qué buscar.
2. La lista o cadena en la que buscará.

**Ejemplo:**

```python
import re
re.findall("ts", "tsnow, tshah, bmoreno")
```

La salida solo será: `['ts', 'ts']` ya que la expresión regular indica que busque cadenas que tienen la secuencia "ts".



