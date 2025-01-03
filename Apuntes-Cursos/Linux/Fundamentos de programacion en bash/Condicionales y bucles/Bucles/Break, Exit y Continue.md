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