# Crear patrones
Se juntan los [[Símbolos]] para crear patrones.

Por ejemplo, si queremos encontrar direcciones de correo de una cadena, podemos crear la expresión regular que filtre por la estructura que conocemos de los correos. correo132@email.com.
- Antes del "@" hay una cadena alfanumérica, se puede representar con *\w+*.
- "@" es un carácter obligatorio, siempre estará presente. Entonces la expresión iría: *\w+@*.
- Tras el "@" va otra cadena que depende del dominio. Puede ser gmail, hotmail, outlook etc: *\w+@\w+*.
- Obligatoriamente va un punto entre el dominio y la extensión. *\w+@\w+\ .* .
- Después va otra cadena que puede ser net, com, co, etc. *\w@\w+\ .\w+* (No hay espacio entre \ y el punto.)

**Ejemplo adicional:**

La siguiente cadena contiene su ID de empleado, su nombre de usuario seguido de dos puntos (:), sus intentos de inicio de sesión del día y su departamento:

```python
employee_logins_string = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"
```

Su tarea consiste en extraer el nombre de usuario y los intentos de inicio de sesión, sin el número de identificación del empleado ni su departamento.

- Nombre de usuario y el ID está antes de los puntos entonces, *\w+:* 
	- El id no se tiene en cuenta en \w porque entre el ID y el nombre de usuario hay un espacio que no especificamos. Si quisiéramos el ID: *\w+\s\w+:*
- Después de los dos puntos hay un espacio entre la cantidad de intentos y el departamento, *\w+\s*
- Tras el espacio está la cantidad de intentos y el departamento pero no necesitamos el departamento (el departamento es una cadena de caracteres la cantidad de intentos son dígitos uno tras otro): *\w+:\s\d+*

```python
import re
pattern = "\w+:\s\d+"

employee_logins_string = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"

print(re.findall(pattern, employee_logins_string))
```

**Salida:** `['bmoreno: 12', 'tshah: 7', 'sgilmore: 5']` 