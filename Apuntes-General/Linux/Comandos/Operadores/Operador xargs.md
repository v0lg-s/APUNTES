## Xargs
El uso de xargs se vuelve útil cuando se desea transformar la salida de un comando (como find) en argumentos individuales para otro comando (como cat). Si se realiza solo con pipe como a continuación se muestra, cat simplemente mostrará en pantalla la entrada desde pipe. Pero si se usa con xargs "cat" tomará lo que viene desde pipe como argumento, por lo que mostrará el contenido del archivo.

```bash
find -name archivo.txt | cat
```

INCORRECTO

```bash
find -name archivo.txt | xargs cat
```

CORRECTO
