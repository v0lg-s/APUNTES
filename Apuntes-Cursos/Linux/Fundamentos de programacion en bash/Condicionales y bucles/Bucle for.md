Sintaxis:
- La sintaxis que se mantiene igual es:
	- El bucle se abre con la palabra `for`.
	- Tras la expresión el ';' es usado de la misma manera que en `if`.
	- Tras el punto y coma la palabra reservada `do` marca el inicio del bloque de código del bucle.
	- Para cerrar el bucle se usa la palabra `done`.

```bash
for variable in {}; do
	#codigo a ejecutar
done
```
- Existen varios tipos de sintaxis para iterar con un bucle, la sintaxis cambia según el caso.
## 1. Iterar en un rango

La sintaxis para este bucle for es:
- El rango está definido por:
	- Inicio
	- Final
	- Paso (Opcional)
- El rango se encuentra entre llaves. '{ }'
- El orden es el siguiente: `'{inicio..final..paso}'` 
- **No puede haber espacios entre las llaves y los rangos.**

```bash
for i in {inicio..final}; do
	echo "For"
done
```

```bash
for i in {2..8..2}; do
	echo "Contar: $i"
done
```

**Resultado:**
Contar: 2
Contar: 4
Contar: 6
Contar: 8
## 2. Iterar en archivos

```bash
#!/bin/bash

for i in file1 file2 file3; do
	echo "Archivo: $i"
done

```
## 3. Iterar sobre la salida de un comando
```bash
#!/bin/bash

for i in $(ls *.txt); do
	echo "Archivo: $i"
done

```

# Break, Exit y Continue

Estas 3 palabras clave son usadas para influir en el flujo del bucle según nuestra necesidad.

- **Break:** Cuando se llega a este comando dentro de cualquier bucle, sale inmediatamente de él y ejecuta la siguiente línea al comando.
- **Continue:** Salta una iteración y continúa a la siguiente.
- **Exit:** Detiene la ejecución del script. Podemos usarlo para devolver un código de estado `$?`.

```bash
#!/bin/bash

for i in $(ls *.txt); do
	echo "Archivo: $i"
	if [ $i = "hola.txt" ]; then
		exit 0
	fi
done
```