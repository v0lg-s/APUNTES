Para comprimir varios archivos en un zip podemos usar el comando zip seguido del nombre que le daremos al archivo comprimido, tras eso escribiremos todos los archivos o directorios que queramos incluir.

```bash
zip saludos.zip hola.pdf buenas.pdf hello.pdf
```

Para descomprimir simplemente usamos el comando unzip seguido del nombre del archivo comprimido.

```bash
unzip saludos.zip
```

Es útil utilizar el comando **7z** este comando es universal para cualquier tipo de comprimido. (.gz, .tar, .bz). Además nos provee de otras utilidades en caso de querer automatizar procesos.

- Opción *l* : Esta opción muestra el contenido del comprimido antes de ser extraído.
- Opción *x* : Con esta opción extraemos el contenido del comprimido.

```bash
7z l archivo.zip
7z x archivo.zip
```

