
> [!NOTE] Algunas excepciones integradas abstractas
> - ArithmeticError,
> - BaseException
> - BaseException,
>- LookupError.
  
> [!NOTE] Algunas excepciones integradas concretas
>- AssertionError,
>- ImportError,
>- IndexError,
>- KeyboardInterrupt,
>- KeyError,
>- MemoryError,
>- OverflowError.

## ZeroDivisionError

Aparece cuando se ejecuta cualquier operación que intente dividir entre cero.

## ValueError

Aparece cuando una función recibe un argumento de un tipo adecuado pero su valor es inaceptable.

**Ejemplo:**
```python
int("soy un número") # Error
```
## TypeError

Aparece cuando se intenta usar un dato cuyo tipo no se acepta en el contexto actual.

**Ejemplo:** 
```python
short_list = [1]
one_value = short_list[0.5] # Error
```

Un índice de punto flotante no se puede dar.

## AttributeError

Aparece cuando se intenta activar un método que no existe en un elemento.

**Ejemplo:**

```python
lista = [1, 2, 3]
lista.append(4)
lista.depend(5) # Error
```

## SyntaxError

Se genera cuando el control llega a una línea que viola la gramática de Python.
Es una *mala idea* manejar este tipo de excepciones en los programas.