**Funciones**
- `random():` produce un flotante entre 0.0 y 1.0. `[0.0 , 1.0)`
- `seed(int_value):` establece la semilla del generador. Sin argumento -> usa la hora actual. 
- `randrange():` Valores aleatorios enteros
	- `randrange(fin)`
	- `randrange(inicio,fin)`
	- `randrange(inicio, fin, incremento)`
	- `randint(izquierda, derecha)` -> no incluye el límite derecho.
- `choice(secuencia):` Elige un elemento 'aleatorio' de la secuencia de entrada.
- `sample(secuencia, elementos_a_elegir):` Crea una lista que consta de los elementos escogidos. Por defecto, es 1.