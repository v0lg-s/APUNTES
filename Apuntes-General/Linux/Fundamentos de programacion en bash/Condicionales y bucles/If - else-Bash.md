La sintaxis básica de un condicional en bash es la siguiente:

- La condición está encerrada entre corchetes '[ ... ]'. Tener en cuenta que debemos separar los corchetes de la condición.
- Tras la condición hay un ';' y la palabra clave `then`.
- Para evaluar un else if se usa la palabra `elif` con la misma estructura del condicional.
- El cierre del condicional se hace con la palabra `fi`.

```bash
if [ condicion ]; then
	echo "Condición verdadera"
elif [ otra condición ]; then
	echo "Otra condición verdadera y la primera falsa."
else
	echo "Ambas condiciones falsa"
fi
```

