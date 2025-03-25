El archivo `/etc/shadow` tiene información de la contraseña de todos los usuarios, en esta se encuentran los campos de:

- **`Contraseña encriptada.`**
	- Si aparece **`!`** o **`*`** la cuenta está bloqueada o desactivada.
- **`Último cambio`**
	- Número de días desde el **1 de enero de 1970** (_epoch time_) en que se cambió la contraseña por última vez.
- **`Días mínimos`**
	- Número de días mínimo para que el usuario pueda cambiar la contraseña.
- **`max_días`**
    - Número máximo de días que la contraseña es válida antes de que se requiera un cambio.
- **`aviso`**
    - Número de días antes de que la contraseña expire en los que el sistema advierte al usuario.
- **`inactividad`**
    - Número de días de inactividad permitidos después de que la contraseña expire antes de que la cuenta se desactive.
- **`expiración`**
    - Fecha en que la cuenta expira (número de días desde el **1 de enero de 1970**).
    - Si está vacío, la cuenta no expira.
- **`reservado`**
    - Campo reservado para uso futuro (normalmente está vacío).

Cada campo está separado por **`:`**.

**Ejemplo**

```plaintext
v0lg:$y$j9T$ORSJc89niFA3fbCj5TjOq0$F5.EYOenM5ajTSK.hf3YU.Wh19fbQx/5P1WrexoYsPC:20045:0:99999:7:::
```