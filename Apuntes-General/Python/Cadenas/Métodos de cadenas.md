
## Pasar primer letra a mayúscula 

- **cadena.capitalize()**
```python
cadena = 'hola, todo estO esTÁ UN pocO desOrdenado'

print(cadena.capitalize()) 
```

Devuelve una cadena con la primer posición (índice 0) en mayus el resto en minúsculas, sin importar si el primer carácter es un carácter no visible.

---
## Centrar cadena

- `cadena.center()`
```python
print('[' + 'alpha'.center(10) + ']')
```

```output
Salida: [  alpha   ]
```

Genera una copia de la cadena original tratando de centrarla en un ancho especificado.

---
## Comprobar si termina con 'x'

- `cadena.endswith("subcadena")`
```python
if "epsilon".endswith("on"):
    print("si")
else:
    print("no")
```

True si la cadena termina con el argumento especificado, False de lo contrario.

---
## Encontrar índice de una subcadena

- `cadena.find("Subcadena")`

```python
print("Eta".find("ta")) # devuelve 1
print("Eta".find("mma")) # devuelve -1
```

Devuelve el índice de la primera aparición de esta subcadena. Si la subcadena no existe dentro de la cadena devuelve `-1`.

**Variante con dos parámetros**
```python
print('kappa'.find('a', 2))
```
Empieza a buscar desde el índice 2 de la cadena.

- `cadena.rfind()`

Busca desde el final de la cadena.

---
## Verificar si una cadena tiene caracteres alfanum
- `cadena.isalnum()`

```python
print('lambda30'.isalnum()) # True
print('lambda'.isalnum()) # True
print('30'.isalnum()) # True
print('@'.isalnum()) # False
print('lambda_30'.isalnum()) # False
print(''.isalnum()) # False
```

Comprueba si la cadena contiene solo dígitos o caracteres alfabéticos.

- `cadena.isalpha()`

Comprueba si la cadena tiene solo letras.

- `cadena.isdigit()`

Comprueba si la cadena tiene solo dígitos.

- `cadena.islower()`

Comprueba si la cadena tiene solo letras minúsculas.

- `cadena.isspace()`

Comprueba si la cadena es de solo espacios en blanco.

- `cadena.isupper()`

Comprueba si la cadena tiene solo letras mayúsculas.

---
## Método join()

El método **realiza una unión** y espera un argumento del tipo lista; se debe asegurar que todos los elementos de la lista sean cadenas.

- Todos los elementos de la lista serán **unidos en una sola cadena**
- La cadena desde la que se ha invocado el método será **utilizada como separador**, puesta entre las cadenas.
- La cadena recién creada se devuelve como resultado.

```python
# Demostración del método join():
print(",".join(["omicron", "pi", "rho"])) # salida: omicron,pi,rho
```

---
## Formato

- `cadena.lower()`

Genera una copia de la cadena pero en minúsculas.

- `cadena.upper()`

Genera una copia de la cadena pero en mayúsculas.

- `cadena.lstrip()`

```python
print("[" + " tau ".lstrip() + "]")
```
Devuelve la cadena sin espacios en blanco.

```python
print("www.cisco.com".lstrip("w."))
```

Hace lo mismo que su versión sin parámetros, pero elimina todos los caracteres incluidos en el argumento (una cadena), no solo espacios en blanco. Solo si están al principio.

- `cadena.rstrip()`

Afecta el lado opuesto de la cadena.

- `cadena.strip()`

Crea una nueva cadena que carece de todos los espacios en blanco iniciales y finales.

## Reemplazar

- `cadena.replace()`

```python
print("www.netacad.com".replace("netacad.com", "pythoninstitute.org"))
print("This is it!".replace("is", "are"))
print("Apple juice".replace("juice", ""))
```

Con dos parámetros devuelve una copia de la cadena original en la que todas las apariciones del primer argumento han sido reemplazadas por el segundo argumento.

Con tres parámetros emplea un tercer argumento (un número) para limitar el número de reemplazos.

## Dividir y crear lista

- `cadena.split()`

```python
print("phi       chi\npsi".split())

# salida ['phi', 'chi', 'psi']
```

Divide la cadena y crea una lista de todas las subcadenas detectadas. El método asume que las subcadenas están delimitadas por espacios en blanco.

## Verificar si inicia con 'x'

- `cadena.startswith()`

```python
print("omega".startswith("meg")) # False
print("omega".startswith("om")) # True
```
Comprueba si una cadena dada comienza con la subcadena especificada.

## Intercambiar mayus y minus

- `cadena.swapcase()`

 Crea una nueva cadena intercambiando todas las letras por mayúsculas o minúsculas dentro de la cadena original: los caracteres en mayúscula se convierten en minúsculas y viceversa.

- `cadena.title()`

 Cambia la primera letra de cada palabra a mayúsculas, convirtiendo todas las demás a minúsculas.
 