# Cómo formular una expresión regular

## \w
El símbolo \w indica cualquier carácter alfanumérico excepto símbolos. Puede ser:
- "1"
- "q"
- "m"

```python
import re
re.findall("\w", "h32rb17")
```

**Salida:** `['h', '3', '2', 'r', 'b', '1', '7']`
## .
El punto "." coincide con cualquier carácter, incluidos simbolos.
- "@"
- "2"
- "m"

## \d
Coincide con cualquier digito simple. [0-9]
- "1"
- "4"
- "8"

```python
import re
re.findall("\d", "h32rb17")
```

**Salida:** `['3', '2', '1', '7']`
## \s
Coincide con todos los espacios simples.
- " "

## \ . 
`\.` coincide con el punto. ".". El carácter del punto.


# Símbolos para cuantificar ocurrencias
## +
El símbolo de suma "+" después de alguno de los simbolos anteriores indica que se puede repetir una o más veces.

**Por ejemplo:** "a+":
- "a"
- "aaa"
- "aa"
- "aaaaaaaaaa"
- Hasta x1000 "a"

```python
import re
re.findall("\d+", "h32rb17")
```

**Salida:** `['32', '17']` 

## *
El símbolo de asterisco sirve para especificar que se puede dar la ocurrencia cero o más veces.

```python
import re
re.findall("\d*", "h32rb17")
```

**Salida:** `['', '32', '', '', '17', '']` Como también coincide con cero apariciones, la Lista contiene ahora cadenas vacías para los caracteres que no eran de un solo dígito numérico.

## { }
Con las llaves especificamos con un número exacto la cantidad de repeticiones a permitir.

```python
import re
re.findall("\d{2}", "h32rb17 k825t0m c2994eh")
```

**Salida:** `['32', '17', '82', '29', '94']` Como coincide con dos repeticiones, cuando Python encuentra un dígito único, comprueba si hay otro a continuación. Si lo hay, Python añade los dos dígitos a la lista y pasa al siguiente. Si no lo hay, pasa al siguiente dígito sin añadir el primer dígito a la lista.

Con las llaves se puede especificar un rango de repeticiones.

```python
import re
re.findall("\d{1,3}", "h32rb17 k825t0m c2994eh")
```

**Salida:** `['32', '17', '825', '0', '299', '4']` 