# Comando chmod
Con este comando tenemos 2 maneras de cambiar los permisos de un archivo.
1. Especificando si hacemos referencia a user (u), group (g) u others (o), y restando los permisos que queremos quitar o sumando los permisos que queremos dar. 

```bash
chmod g+wx,o-r archivo.txt
```

En este caso, estamos dando al grupo el permiso de escritura y ejecución sobre el archivo "archivo.txt". Y quitando el permiso de lectura a Other.

2. Usando decimales para especificar que permisos dar sin especificar si a user, group u others.
```bash
chmod 604 archivo.txt
```

Esto le da permisos de lectura y escritura a user, le quita los permisos a group y le da permiso de lectura a others sobre el archivo "archivo.txt".

