Mostrar cosas en pantalla.

**Impresión multilínea:**
```python
print(
"""
+================================+
| ¡Bienvenido a mi juego, muggle!|
| Introduce un número entero     |
| y adivina qué número he        |
| elegido para ti.               |
|¿Cuál es el número secreto?     |
+================================+
""")
```
# Argumentos de palabra clave

## end
- **end:** Determina qué caracteres se envían a la salida cuando *print* llega al final de sus argumentos posicionales.
```python
  print("Hola ", end="FINAL ")
  print("Otra salida")
  ```
Esto producirá: *Hola FINAL Otra salida*
## sep
- **sep:** Determina qué caracter/caracteres se usarán para separar los argumentos posicionales.
```python
print("Prueba", "1", "2", "Final de la prueba", sep="-")
```
Producirá: *Prueba-1-2-Final de la prueba*
