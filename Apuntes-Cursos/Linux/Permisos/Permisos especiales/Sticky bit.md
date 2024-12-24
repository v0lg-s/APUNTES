Su función principal es **controlar los permisos de eliminación de archivos dentro de un directorio compartido**.

- El objetivo de este bit es que solo el usuario creador pueda eliminar o renombrar un archivo
- Cuando el *Sticky bit* se configura en un directorio, los archivos dentro de este solo podrán ser *eliminados* o *renombrados* por el usuario que creó el archivo y el usuario `root`. 
- El *Sticky bit* se representa por una ***'`t`'*** o **'`T`'** y se muestra en el bit de permisos de ejecución del grupo de bits de [[Tipos de permisos y Usuarios#3. Otros/Other|Other]].

- **`t`**: Sticky Bit activado, permisos de ejecución para otros.
- **`T`**: Sticky Bit activado, sin permisos de ejecución para otros (menos común).

**Nota:** Solo es aplicable a directorios.

```bash
chmod +t directorio
```

**Ejemplo:** El directorio `/tmp` tiene activo el sticky bit.
```bash
ls -ld /tmp
```

# Notación octal
El sticky bit en notación octal de permisos es un 1 o 0 al principio.

**Ejemplo:**

```bash
chmod 0777 directorio
```

Sticky bit desactivado (Todos los permisos especiales se desactivan).

```bash
chmod 1777 directorio
```

Sticky bit activado.