# Leer primera parte de un archivo muy grande.

## Comando head
Este comando nos permite especificar cuantas lineas de texto desde arriba del documento deseamos ver.

```bash
head -n 10 nombre_archivo
```

La opción "-n" indica que lo siguiente que vamos a enviar como argumento es la cantidad de lineas que queremos ver del archivo en cuestión. En este caso, se van a mostrar 10 lineas del inicio del documento.

La opción "-c" indica que el argumento a continuación es la cantidad de bytes que queremos ver del inicio del archivo.

# Leer última parte de un archivo.

## Comando tail
Este comando nos permite especificar la cantidad de lineas, bytes, etc; desde el final del documento ,que deseamos ver.

```bash
tail -n 5 nombre_archivo
```

Podemos ver las opciones del comando con "man tail".

