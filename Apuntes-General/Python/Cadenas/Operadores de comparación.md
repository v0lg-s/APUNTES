- `==`
    - `True` si ambas cadenas tienen **misma longitud** y **mismos caracteres en el mismo orden** (coincidencia exacta).
        
- `!=`
	- `True` si **no** son exactamente iguales (difiere algún carácter o la longitud).
    
- `>`
    - Compara **lexicográficamente** (carácter por carácter).
	- En el **primer** carácter diferente, decide por su valor Unicode (`ord`).
	- Si una es prefijo de la otra, la **más larga** es mayor (ej. `"abcde" > "abc"`).
	- Ejemplo: `print("13" > "123")` → `True` (porque `'1'=='1'` y luego `'3'>'2'`)
        
- `>=`
    - `True` si es mayor o igual (misma regla de `>` o igualdad total).
    - Ejemplo: `print("13" >= "13")` → `True`
        
- `<`
    - Igual que `>`, pero al revés: menor en el primer carácter distinto; si una es prefijo de la otra, la más corta es menor.
    - Ejemplo: `print("10" < "212")` → `True` (porque `'1'<'2'` desde el primer carácter)
        
- `<=`
    - `True` si es menor o igual.
    - Ejemplo: `print("112" <= "13")` → `True` (porque `'1'=='1'` y luego `'1'<'3'`)