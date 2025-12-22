
# Variable \_\_name__
La variable \_\_name__  es una variable especial que indica cómo se está ejecutando un script:

- Cuando se ejecuta un archivo directamente, su variable `__name__` se establece a `__main__`;
- Cuando un archivo se importa como un módulo, su variable `__name__` se establece al ``nombre del archivo`` (excluyendo a .py)

**Ejemplo**
```python
# desde un archivo llamado modulo.py
print("soy un modulo")
if __name__ == "__main__":
    print("estoy ejecutandome directamente")
else:
    print("estoy siendo importado")

# desde un archivo llamado main.py que importa module
import modulo 
# cuando se ejecuta, python ejecuta una vez el módulo para recordar sus entidades
# entonces, la salida es: "estoy siendo importado"

```


# Variable path
Almacena todas las ubicaciones (carpetas o directorios) que se buscan para encontrar un módulo que ha sido solicitado por la instrucción import.

```python
import sys

for p in sys.path:
  print(p)
```

```console
c:\Users\user\Desktop\Conocimiento\PYTHON\py\progs
C:\Python314\python314.zip
C:\Python314\DLLs
C:\Python314\Lib
C:\Python314
C:\Users\user\AppData\Roaming\Python\Python314\site-packages
C:\Python314\Lib\site-packages
```