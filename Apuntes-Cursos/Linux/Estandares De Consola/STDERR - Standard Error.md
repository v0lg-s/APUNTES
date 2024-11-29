- 2 → (Standard Error)

Son los errores que se obtienen al ejecutar un comando.

También podemos imaginarlo como un recipiente en el que podemos poner cosas. Cuando los comandos generan un error envían sus errores al recipiente stderr.

El número es un código que podemos usar para hacer referencia a este "recipiente" desde la terminal.

Por ejemplo, 

```bash
cat archivo_inexistente.txt 2>errores_generados.txt
```

De esta manera, estaríamos redirigiendo los errores del comando a un archivo de texto. Podemos enviarlos también a /dev/null que es como una papelera para enviar cosas que no necesitamos. (Se borrarán instantaneamente)

Se encuentra en la ruta /dev/stderr

Podemos enviar cosas entre todos los estándares. Por ejemplo, si queremos que se muestre un error en la terminal enviamos el stderr al stdout.

```bash
cat archivo_inexistente.txt 2>&1
```
