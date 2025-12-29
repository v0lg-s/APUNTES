# setfirstweekday()

Esta función permite cambiar el primer día de las semanas en la visualización de los calendarios.

```python
import calendar

calendar.setfirstweekday(calendar.SUNDAY)
calendar.prmonth(2020, 12)
```

```console
   December 2020
Su Mo Tu We Th Fr Sa
       1  2  3  4  5
 6  7  8  9 10 11 12
13 14 15 16 17 18 19
20 21 22 23 24 25 26
27 28 29 30 31
```

# Función weekday()

Esta función devuelve el día de la semana como un valor entero para el año, mes y día especificados.

0 - Lunes $\rightarrow$ 6 - Domingo

```python
import calendar
print(calendar.weekday(2020, 12, 24)) # salida: 3: Jueves
```

# Función weekheader()

Esta función muestra la cabecera de las semanas, su argumento es la separación entre los nombres de los días.

```python
import calendar
print(calendar.weekheader(10))
```

Salida:
```
  Monday    Tuesday   Wednesday   Thursday    Friday    Saturday    Sunday
```

# Función isleap() y leapdays()
La función `isleap()` devuelve `True` si el año enviado como argumento es un año bisiesto, `False` de lo contrario.

La función `leapdays()`, devuelve el número de años bisiestos en un rango de años dado.

```python
import calendar

print(calendar.isleap(2020))
print(calendar.leapdays(2010, 2021))  # Hasta 2021, pero sin incluirlo.
```