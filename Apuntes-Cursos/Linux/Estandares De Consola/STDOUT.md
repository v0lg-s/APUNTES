- 1 → (Standard Output)

Son las salidas que se obtienen de un comando.

También podemos imaginarlo como un recipiente en el que podemos poner cosas. De hecho, los comandos envían su salida a stdout y la terminal muestra lo que se encuentra en stdout en el momento por defecto.

El número es un código que podemos usar para hacer referencia a este "recipiente" desde la terminal.

Por ejemplo, 

```bash
ls -al 1>archivo_salida.txt
```

Es equivalente al comando
```bash
ls -al > archivo_salida.txt
```

Se encuentra en la ruta /dev/stdout