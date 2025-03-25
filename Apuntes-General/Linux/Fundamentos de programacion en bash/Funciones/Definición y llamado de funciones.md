Para definir una función:

```bash
mi_funcion(){
	echo "Hola desde mi función"
}
```

Para llamar a la función:

```bash
mi_funcion
```

Para una funcion con parámetros:

```bash
suma(){
	echo "Total: $(( $1 + $2 ))"
}

suma 5 10
```

