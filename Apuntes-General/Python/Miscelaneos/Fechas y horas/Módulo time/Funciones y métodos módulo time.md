# Método sleep()
Suspende la ejecución del programa por la cantidad de segundos indicada como argumento.

```python
import time

class Student:
    def take_nap(self, seconds):
        print("Estoy muy cansado. Tengo que tomar una siesta. Hasta luego.")
        time.sleep(seconds)
        print("¡Dormí bien! ¡Me siento genial!")

student = Student()
student.take_nap(5)
```


# Método ctime()

Convierte timestamps en segundos a una cadena que tiene formato:  "Día de la semana - Mes -  Fecha - Hora - Año"

```python
import time

timestamp = 1572879180
print(time.ctime(timestamp))
```

Sin un argumento, va a devolver la fecha y hora locales en dicho formato.

