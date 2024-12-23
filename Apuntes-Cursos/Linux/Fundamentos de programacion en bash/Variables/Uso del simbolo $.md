En bash se usa el signo '$' para acceder al valor de una variable antes declarada.

```bash
nombre="Jose"
echo $nombre
```

Es una buena práctica usar comillas:

```bash
echo "$nombre"
```

## Gestión de variables vacías o no definidas

- Dar un valor por defecto si la variable está vacía:

```bash
echo ${nombre:-"Valor por defecto"}
```

- Asignar un valor por defecto si está vacía:

```bash
echo ${nombre:="Valor asignado"}
```

- Mostar mensaje si la variable está vacía:

```bash
echo ${nombre:?"Error, variable vacía"}
```


## Ejecución de comandos
Usar el simbolo *'$'* junto a *'(...)'* permite ejecutar un comando y devolver su salida. Útil para tomar salidas de la consola y asignarlas a variables.

**Ejemplo 1**
```bash
usuario=$(whoami)
```

**Ejemplo 2**
```bash
for archivo in $(ls *.txt); do
	echo "Archivo: $archivo"
done
```

## Cálculos aritméticos
Usando el símbolo *'$'* junto a *'((expresión))'* realiza la evaluación de la expresión aritmética.

```bash
suma=$((5 + 3))
echo "Resultado: $suma"
```