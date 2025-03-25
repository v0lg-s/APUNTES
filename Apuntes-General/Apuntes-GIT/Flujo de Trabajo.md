
1. Con el comando *"git add"* se seleccionan en una primera instancia los archivos que se desean subir al repositorio. Estos pasan a *"stage"* y no se verán reflejados los cambios en el repositorio aún.
2. Con el comando de *"git commit"* estos archivos pasan a la etapa de *"commit"*, y se eliminan de la etapa intermedia de *"stage"*. 
3. Con el comando de *"git push"* se envían los archivos al servidor, puede ser github u otros.

![[stagesGIT.png]]

Para eliminar archivos se corre el mismo flujo "enviando" el archivo que se está eliminando para tener registro de este archivo en el historial del repositorio.

