El comando useradd añade un usuario al sistema. 
- Solo el usuario Root o usuarios con privilegios SUDO pueden ejecutar este comando.

**OPCIONES**
- -g: Establece el grupo por defecto del usuario, también llamado su grupo primario
```bash
sudo useradd -g security fgarcia
```
Se creó el usuario fgarcia y se añadió al grupo security.
- -G: Añade al usuario a grupos adicionales, también llamados grupos suplementarios o secundarios
```bash
sudo useradd -G finance,admin fgarcia
```
Se creó el usuario fgarcia y se añadió a grupos suplementarios.
