La clase `datetime` del módulo con su mismo nombre, puede representar la fecha y la hora como un solo objeto o como objetos separados.

```python
datetime(year, month, day, hour, minute, second, microsecond, tzinfo, fold)
```

# Métodos para fecha y hora actual

La clase `datetime` tiene métodos como:

- `today()` - devuelve la fecha y hora actual con el atributo `tzinfo` establecido a `None`.
- `now()` - devuelve la fecha y hora local actual igual que el método _today_ 
- `utcnow()` - devuelve la fecha y hora UTC actual con el atributo _tzinfo_ establecido a _None_.

```python
from datetime import datetime

print("hoy:", datetime.today())
print("ahora:", datetime.now())
print("utc_ahora:", datetime.utcnow())
```

# Calcular timestamp

Se puede a partir de un objeto de tipo `datetime` obtener la marca de tiempo en función de su fecha y hora con el método `timestamp()`.

```python
from datetime import datetime

dt = datetime(2020, 10, 4, 14, 55)

print("Timestamp:", dt.timestamp()) # Timestamp: 1601823300.0
```

*Recordar*: Número de segundos transcurridos entre la fecha y la hora indicadas por el objeto _datetime_ y el 1 de enero de 1970, 00:00:00 (UTC).