# Operador de re-dirección (redirect >)
Este operador se usa para escribir en un archivo la salida de un comando en terminal. 
"Redirige" la salida de un comando a donde nosotros especifiquemos. El operador es ">".

```bash
echo "Hola mundo" 
```

El comando anterior mostrará como salida "Hola mundo" en la terminal. Podemos redirigir esta salida a un archivo.

```bash
echo "Hola mundo" > holaMundo.txt
```

Esto creará un archivo con el nombre "holaMundo.txt" en el directorio en el que estemos trabajando y contendrá la salida del comando, es decir, "Hola mundo".

# Operador "pipe |"
Este operador redirige la salida de un comando para usarla como argumento de otro comando.

```bash
ls -al | less 
```

Envía la salida del comando "ls -al" al comando "less" que se encarga de mostrar el contenido en una pagina para que archivos grandes de texto sean más fáciles de leer.

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
