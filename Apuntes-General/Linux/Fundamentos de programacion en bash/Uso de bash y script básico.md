Bash es útil para:
- Automatizar tareas repetitivas.
- Administrar sistemas y servidores.
- Procesar archivos y datos rápidamente.

# ¿Qué es necesario para crear un script?

- El programa se almacenará en un archivo con la extensión *'.sh'*.
- La primer línea del programa debe ser:

```bash
#!/bin/bash
```

(Línea shebang) Es utilizada para indicarle al sistema qué interprete usar cuando ejecutemos el archivo. `#!/'ruta/al/interprete'`

- Es necesario hacer ejecutable el archivo.

```bash
chmod +x script.sh
```

Tener cuidado con lo anterior, lo hace ejecutable para todos los usuarios. *'Grupo y otros.'*

- Para ejecutarlo se escribe su nombre.

```bash
./script.sh
```

