El archivo `/etc/passwd` tiene información de todos los usuarios, en esta se encuentran los campos de:
- User ID. 
	- **0** para el usuario *root*
	- **1-99** para usuarios del sistema (servicios)
	- **1000+** usuarios normales
- Group ID.
- Comentarios.
- Directorio personal del usuario.
- Ruta al Shell predeterminado que se inicia al iniciar sesión.

**Ejemplo:**

```plaintext
v0lg:x:1000:1000:v0lg,,,:/home/v0lg:/usr/bin/zsh
```

- La x indica que la contraseña está cifrada y se guarda en `/etc/shadow`
- **UID:** 1000
- **GID:** 1000
- **Comentarios:** Nombre del usuario
- **Directorio personal:** `/home/volg`
- **Shell predeterminada:** `/usr/bin/zsh`


