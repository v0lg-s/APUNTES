Este bucle se ejecutará mientras la condición sea verdadera.

Su sintaxis:

- Inicia con la palabra reservada `while`.
- La condición va seguida de la palabra `while` y de la misma manera que con el condicional `if`, va dentro de corchetes '[ ... ]'. **La condición debe ir separada de los corchetes.** 
- Tras la condición ';' y la palabra reservada `do`.
- Para cerrar el bucle while se usa la palabra reservada `done`.

```bash
contador=1
while [ $contador -le 5 ]; do
	echo "Contador: $contador"
	let contador++
done
```

