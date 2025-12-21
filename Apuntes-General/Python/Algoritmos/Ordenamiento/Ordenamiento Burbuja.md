Se usa raramente, es fácil de entender pero poco eficiente. No útil para listas extensas.

De una lista de elementos queremos ordenarlos (de forma ascendente o descendente).

1. Tomamos el primer y segundo elemento de la lista y los comparamos, si el primero es mayor al segundo, intercambiamos su posición; de lo contrario, si su orden es válido no hacemos nada.
2. Se vuelve a iterar hasta que no hay más por ordenar.

Esto se puede lograr con dos bucles, un bucle while y un bucle for:

Supongamos una lista con *n* elementos:

El bucle for recorre la lista hasta el penúltimo elemento (n-1), ya que irá comparando de a parejas. Si llegase al último elemento, no tendría con cual comparar, porque no existe un elemento n+1.

```python
list = [8, 10, 6, 2, 4]

for i in range(len(list)-1): 
	if list[i] > list[i+1]:
		list[i], list[i+1] = list[i+1], list[i]
```

Este bucle for sería *solamente* la ejecución del primer paso, tenemos que revisar si hay otros números que no estén en su posición correcta, para esto usaremos el bucle While con una variable auxiliar.

```python
lista = [8, 10, 6, 2, 4]

swapped = True

while swapped:
	swapped = False
	for i in range(len(lista)-1): 
		if lista[i] > lista[i+1]:
			swapped = True
			lista[i], lista[i+1] = lista[i+1], lista[i]
			
print(lista)
```

La variable *swapped* nos indica si hubo intercambios en la lista.

Si luego de una iteración su valor se mantiene en *False*, indica que no hubo ningún intercambio por lo que la lista ya está ordenada, por eso sale del bucle while.

Si luego de una iteración su valor pasa a *True*, indica que la lista no estaba ordenada y hubo un intercambio, por lo que continuamos en el bucle para que en la siguiente iteración se verifique si la lista ya se ordenó con ese cambio.