Cuando realizamos cambios en el proyecto con un repositorio ya inicializado podemos (dentro del directorio del repositorio) ejecutar el comando *"git status"*.

## Comando git status
Nos mostrará por pantalla el estado del proyecto, si hay cambios en el proyecto que no se han enviado a la etapa de stage (archivos borrados, modificados, agregados) nos dará un listado de estos.

![[git-STATUS.png]]

# Archivo modificado/eliminado del proyecto
Cuando eliminamos o modificamos un archivo del proyecto en cuestión, debemos realizar de nuevo un *"git add"* de estos archivo para pasarlos a la etapa de "stage".

![[git-add.png]]

# Sacar archivo de la etapa stage
Si por alguna razón queremos sacar un archivo de la etapa de stage, podemos ejecutar el siguiente comando:

```bash
git restore --staged archivo.json
```

# Restaurar cambios
Si queremos deshacer los cambios hechos en un directorio sobre un archivo podemos usar el siguiente comando:

```bash
git restore archivo.json
```