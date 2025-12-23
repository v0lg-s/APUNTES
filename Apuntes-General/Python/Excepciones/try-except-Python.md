**Regla para manejar los errores en python:** "Es mejor manejar un error cuando ocurre que tratar de evitarlo." se basa en "Es mejor pedir perdón que permiso"

```python
try:
	# aquí se coloca 
	# el codigo que se sospecha 
	# con riesgo de terminar con error.
except:
	# Es un espacio dedicado  
    # exclusivamente para "pedir perdón".
    # aquí se maneja el error.
```

Se pueden capturar diferentes excepciones, se debe especificar el nombre de la excepción que se quiere manejar:

```python
try:
    value = int(input('Ingresa un número natural: '))
    print('El recíproco de', value, 'es', 1/value)        
except (ValueError, AnyError, AnyAnyError): # asi se ponen multiples excepciones
    print('Dato incorrecto')    
except ZeroDivisionError:
    print('La división entre cero no está permitida en nuestro Universo.') 
except:
	print('Error no contemplado')
```

Si declaramos la sentencia `except` sin un nombre de excepción, serán estas instrucciones las que se ejecuten si se levanta un error distinto a los que ya configuramos. Excepción predeterminada.

**Nota:** el `except` por defecto debe ser el último except.