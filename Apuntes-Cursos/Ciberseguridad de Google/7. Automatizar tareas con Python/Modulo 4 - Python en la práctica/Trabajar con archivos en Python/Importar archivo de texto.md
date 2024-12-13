Para abrir un archivo de texto se usan varias palabras clave:
- **with:** Esta palabra clave o sentencia maneja errores y gestiona los recursos cuando se utiliza con otras funciones. Cuando se usa con *open()* para abrir un archivo. Una vez finalice la ejecución local de la sentencia with, esta gestionará los recursos para cerrar de manera correcta el archivo abierto.
- **open():** Esta función abre un archivo en Python.
	- El primer parámetro es la dirección absoluta del archivo. (Si el archivo está en el mismo directorio que el archivo Python se puede acceder a este solo con el nombre).
	- El segundo parámetro indica lo que se desea hacer con el archivo. *r* para *read*, *w* para *write* y *a* para *anexar*.
- **as:** Esta palabra clave asigna una variable que hace referencia al archivo abierto en este caso. Después de ella se indica el nombre de la variable que queremos asignarle al objeto del archivo.

```python
with open("archivo.txt","r") as file:
	# otras sentencias
```

Todo lo que hagamos con el archivo lo hacemos dentro de la sentencia *with*.

Dado que creamos un objeto del tipo archivo tenemos métodos asociados:

**Por ejemplo:** Podemos usar el método *.read()* para leer el contenido del archivo. El método *.read()* convierte los archivos en cadenas. Esto es necesario para poder utilizar y mostrar el contenido del archivo que se ha leído.

```python
with open("archivoDeActualizaciones.txt","r") as archivo:
	actualizaciones = archivo.read()
print(actualizaciones)
```


# Escribir en un archivo desde Python
Para escribir en el archivo cambiamos el argumento *r* por el de *w* o *a* en la función *open()*.

- **w:** Sustituye el contenido de un archivo existente. Si no existe el archivo en la dirección absoluta dada, el parámetro *w* lo crea.
- **a:** Añade nueva información al final de un archivo existente.

Tanto *a* como *w* usan el método *.write()* para escribir en el archivo. **Ejemplo:**

```python
lineaNueva = "jrafael,192.168.243.140,4:56:27,True"

with open("access_log.txt", "a") as file:
    file.write(lineaNueva)
```

