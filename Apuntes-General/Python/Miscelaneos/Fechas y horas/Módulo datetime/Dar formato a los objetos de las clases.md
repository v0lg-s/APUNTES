Todas las clases de `datetime` presentes en estos apuntes tienen un método llamado `strftime()`, permite devolver la fecha y hora en el formato que especifiquemos.

El método strftime toma solo un argumento en forma de cadena que especifica un formato que puede constar de directivas.

Una directiva es una cadena que consta del carácter % (porcentaje) y una letra minúscula o mayúscula. Por ejemplo, la directiva %Y significa el año con el siglo como número decimal.

```python
from datetime import date

d = date(2020, 1, 4)
print(d.strftime('%Y/%m/%d'))
```

Directivas: https://docs.python.org/3/library/datetime.html#strftime-and-strptime-format-codes 

# En el módulo time
El módulo time usa este método y tiene una opción adicional, recibe un objeto tuple o struct_time.

```python
import time

timestamp = 1572879180
st = time.gmtime(timestamp)

print(time.strftime("%Y/%m/%d %H:%M:%S", st))
print(time.strftime("%Y/%m/%d %H:%M:%S"))
```

Directivas módulo time: https://docs.python.org/3/library/time.html#time.strftime