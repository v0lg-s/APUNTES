Set user ID.

- El bit SetUID se utiliza para elevar temporalmente los privilegios de un usuario.
- Cuando el bit *SetUID* se configura en un archivo ejecutable, permite que al ejecutarse corra con los permisos del usuario propietario, no el usuario que lo ejecutó.
- El bit de *SetUID* se representa por una *'s'* y se muestra en el bit de permisos de ejecución del grupo de bits de [[Tipos de permisos y Usuarios#1. Usuario/User|User]].

**Nota:** Solo es aplicable a archivos ejecutables.

**Por ejemplo:**
En Linux el comando `passwd` tiene el bit setuid activo.

![[SetuidPasswd.png]]

Es por esto que el comando `passwd` nos permite cambiar la contraseña del usuario actual (modificando el archivo /etc/shadow protegido) sin tener permisos de super usuario.

- Ejecutamos `passwd` y se ejecuta con los permisos del usuario propietario del archivo, en este caso `root`.

Hay que asegurarse que los procesos que realmente necesiten este permiso sean los únicos con el bit *SetUID* activado, dado que asignar este bit de forma indiscriminada puede ser un riesgo grave de seguridad.

Se activa el bit mediante el comando [[Apuntes-Cursos/Linux/Permisos/Cambiar Permisos|chmod]]  de la misma manera en que cambiamos los permisos.

```bash
chmod u+s
chmod u-s
```

Es necesario que el archivo también tenga permisos de ejecución.

# Notación octal
El bit *SetUID* en notación octal de permisos es un 2 o 0 al principio.

**Ejemplo:**

```bash
chmod 0777 directorio
```

*SetUID* desactivado (Todos los permisos especiales se desactivan)

```bash
chmod 2777 directorio
```

*SetUID* activado