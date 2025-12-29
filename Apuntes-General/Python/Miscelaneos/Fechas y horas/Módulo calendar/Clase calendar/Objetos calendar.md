El constructor de un objeto calendar recibe como argumento el día de la semana que se va a mostrar primero en los calendarios. Lunes = 0 por defecto.

```python
import calendar  

c = calendar.Calendar(calendar.SUNDAY)

for weekday in c.iterweekdays(): # itera en los días de la semana desde el primer 
    print(weekday, end=" ") # día definido

# salida: 6 0 1 2 3 4 5
```

# Métodos

## Método itermonthdates()

El método `itermonthdates`, requiere especificar el año y el mes. Se devuelven todos los días del mes y año especificados, así como todos los días antes del comienzo del mes o del final del mes que son necesarios para obtener una semana completa.

Cada día está representado por un objeto `datetime.date`.

```python
import calendar  

c = calendar.Calendar()

for date in c.itermonthdates(2019, 11):
    print(date, end=" ")
```

```
2019-10-28 2019-10-29 2019-10-30 2019-10-31 2019-11-01 2019-11-02 2019-11-03 2019-11-04 2019-11-05 2019-11-06 2019-11-07 2019-11-08 2019-11-09 2019-11-10 2019-11-11 2019-11-12 2019-11-13 2019-11-14 2019-11-15 2019-11-16 2019-11-17 2019-11-18 2019-11-19 2019-11-20 2019-11-21 2019-11-22 2019-11-23 2019-11-24 2019-11-25 2019-11-26 2019-11-27 2019-11-28 2019-11-29 2019-11-30 2019-12-01
```

## Método itermonthdays()

Este método toma año y mes como parámetros, y luego devuelve el iterador a los días de la semana representados por números.

```python
import calendar  

c = calendar.Calendar()

for iter in c.itermonthdays(2019, 11):
    print(iter, end=" ")
```

```
0 0 0 0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 0
```

La gran cantidad de ceros devueltos como resultado son días fuera del intervalo de meses especificado que se agregan para mantener la semana completa.