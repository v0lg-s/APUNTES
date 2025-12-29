La clase `timedelta` del módulo `datetime` fue creada con el propósito de hacer operaciones con las fechas y horas.

Un objeto `timedelta` se crea cuando se restan dos objetos de `date` o `datetime`

```python
from datetime import date
from datetime import datetime

d1 = date(2020, 11, 4)
d2 = date(2019, 11, 4)

print(d1 - d2) # 

dt1 = datetime(2020, 11, 4, 0, 0, 0)
dt2 = datetime(2019, 11, 4, 14, 53, 0)

print(dt1 - dt2)
```

Salida:

```bash
366 days, 0:00:00

365 days, 9:07:00
```

# Creación de objetos timedelta

El constructor de un objeto `timedelta` recibe los siguientes argumentos opcionales.

```python
(days, seconds, microseconds, milliseconds, minutes, hours, weeks)
```

Números enteros o de punto flotante y positivos o negativos.

```python
from datetime import datetime

delta = timedelta(weeks=2, days=2, hours=2)
print(delta)

delta2 = delta * 2
print(delta2)

d = date(2019, 10, 4) + delta2
print(d)

dt = datetime(2019, 10, 4, 14, 53) + delta2
print(dt)
```

Salida:

```console
16 days, 2:00:00

32 days, 4:00:00

2019-11-05

2019-11-05 18:53:00
```