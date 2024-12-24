Set Group ID.

Es de utilidad cuando varios usuarios pertenecientes a un grupo deben realizar sus tareas utilizando los recursos ubicados dentro de un mismo directorio.

- El bit *SetGID* se utiliza para que un determinado proceso adquiera los privilegios del **grupo** al que ha sido asignado un fichero o directorio.
- El bit de *SetGID* se representa por una *'s'* y se muestra en el bit de permisos de ejecución del grupo de bits de [[Tipos de permisos y Usuarios#2. Grupo/Group|Group]].

**Nota:** Es aplicable tanto a ficheros como directorios.

# Bit setgid aplicado a ficheros
- En un archivo ejecutable con el bit *SetGID* activo:
	- El archivo será ejecutado con los permisos del grupo al que pertenece el archivo.

# Bit setgid aplicado a directorios
- En un directorio con el bit *SetGID* activo:
	- El conjunto de archivos y directorios dentro de este tendrán el mismo grupo que el del directorio principal, en lugar del grupo del usuario creador del archivo.
## Ejemplo

**Situación:**
Existe un directorio uso compartido llamado `/compartido` sin el bit *SetGID* activo.

```bash
mkdir compartido
chmod g+wx compartido
chmod o-rx compartido
```

Los permisos de este directorio serán:
`drwxrwx---` 

Los propietarios de este directorio son:
- **User:** root
- **Group:** grupo1

En el sistema hay dos usuarios pertenecientes al `grupo1`:
- **user1**
- **user2**

Si el usuario `user1` crea el archivo prueba.txt en el directorio `/compartido`. La propiedad de este archivo será:
- **User:** user1
- **Group:** user1
Y si sus permisos son:
`-rwxrwx---` 

Por lo que si el usuario `user2` quisiera leer lo que hay dentro de este archivo compartido NO tendría los permisos requeridos.

Para solucionar esto activamos el bit de *SetGID* en el directorio `/compartido`:

```bash
chmod g+s compartido
```

Los permisos de este directorio serán:
`drwxrws---` 

Ahora, si se vuelve a realizar el mismo procedimiento:
- Usuario `user1` crea el archivo prueba.txt en el directorio `/compartido`. La propiedad de este archivo será:
	- **User:** user1
	- **Group:** grupo1
- Y si sus permisos son: `-rwxrwx---` 

Dado que ahora el archivo prueba.txt es propiedad del grupo `grupo1`, el usuario `user2` (perteneciente al `grupo1`) puede leer, escribir o ejecutar este archivo.

# Notación octal
El bit *SetGID* en notación octal de permisos es un 4 o 0 al principio.

**Ejemplo:**

```bash
chmod 0777 directorio
```

*SetGID* desactivado (Todos los permisos especiales se desactivan)

```bash
chmod 4777 directorio
```

*SetGID* activado