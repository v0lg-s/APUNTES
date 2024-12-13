Es el proceso de convertir los datos a un formato más legible. Esto puede ocurrir de dos maneras, primero que los datos necesiten estar en cierto formato para poderlos procesar con Python de cierta manera, o segundo, que el programador necesite que los datos estén con una estructura más clara y legible para poderlos analizar.

# Métodos de parsing
Entre los métodos usados para cambiar la estructura o formato de datos en Python se encuentran:
- .split()
- .join()

## .split()
Este método convierte una cadena en una lista. Separa la cadena en función de un carácter especificado en un parámetro, si este parámetro no se especifica, el método creará los elementos de la lista separando la cadena cada vez que encuentre un espacio en blanco.

**Ejemplo:**
```python
usuarios_aprobados = "elarson,bmoreno,tshah,sgilmore,eraab"
usuarios_aprobados = usuarios_aprobados.split(",") # Separa la cadena cada vez que encuentre una coma ","
print("Lista de usuarios",usuarios_aprobados)
```

**Salida:** `Lista de usuarios ['elarson', 'bmoreno', 'tshah', 'sgilmore', 'eraab']` 

## .join()
Este método realiza el proceso contrario a .split(), toma una lista o cualquier elemento iterable y concatena los elementos en una cadena.

- El método join utiliza una sintaxis distinta a los anteriores.
- Este método recibe como argumento la lista que se desea concatenar a una cadena.
- El método se añade frente al carácter con el que queramos separar cada elemento de la lista al concatenarlo.

```python
usuarios_aprobados = ["elarson", "bmoreno", 'tshah', "sgilmore", "eraab"]
usuarios_aprobados = ",".join(usuarios_aprobados)

print("Cadena:",usuarios_aprobados)

```

**Salida:** `Cadena: elarson,bmoreno,tshah,sgilmore,eraab`

**Nota:** Para añadir un salto de línea entre los elementos podemos usar *"\n"* 