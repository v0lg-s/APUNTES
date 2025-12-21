Esta operación es también conocida com **Shifting** . Se aplica únicamente a los valores de *número entero*.

El desplazamiento es esencialmente la multiplicación por potencias de la base del sistema que estemos usando.

**Ejemplo en sistema decimal**
- `12345 x 10 = 123450` Multiplicar por 10 es un desplazamiento de los dígitos a la izquierda y llenar el vacío con un cero. `<<`
- `12345 / 10 = 1234` Dividir por 10 es un desplazamiento de los dígitos a la derecha y descartar el menos significativo. `>>`

En el sistema binario, dado que la base de este sistema es el 2, desplazar bits logra realizar multiplicaciones o divisiones por potencias de dos.

```python
valor << bits # corrimiento a la izquierda
valor >> bits # corrimiento a la derecha
```

*Ejemplo*

```python
num = 10 # equivalente de 1010 en binario

multiply = num << 3 # En esta caso estamos multiplicando 10 en decimal por 2^3

print(multiply) # multiply: 1010000 -> 80 en decimal. 10 x (2^3) = 80
```

