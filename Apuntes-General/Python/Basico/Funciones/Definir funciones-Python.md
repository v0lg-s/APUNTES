Las funciones en python se definen con la palabra clave `def`.

```python
def message():
	print("Ingresa un valor: ")
	

message() # invocacion de la función
```

# Variables y alcance dentro de una función 

Las variables definidas dentro de una función no son accesibles globalmente.

```python
def function():
	var = 23
	print("Variable local: ",var)
	
print("Variable de la funcion: ",var) # esto produce un error
```

Pero las variables definidas en el entorno global son accesibles desde dentro de una función.
## Variables globales

`global` es un método especial de python nos permite extender el alcance las variables.

```python
def my_function():
    global var
    var = 2
    print("¿Conozco a aquella variable?", var)


var = 1
my_function()
print(var)
```

