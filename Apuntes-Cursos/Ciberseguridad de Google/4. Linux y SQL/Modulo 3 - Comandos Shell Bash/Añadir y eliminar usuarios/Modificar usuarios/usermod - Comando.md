El comando usermod modifica las cuentas de usuario existentes. Mismas opciones de -g y -G que en useradd.

**OPCIONES**
- **-g:** Cambia el grupo principal del usuario.
- **-a -G:** Se utiliza -a antes de -G para que al añadir un grupo a los suplementarios del usuario no se sobrescriban los grupos a los que ya pertenece.
- **-d:** Cambia el Directorio personal del usuario.
```bash
sudo usermod -d /home/garcia_f fgarcia
```
- **-l:** Cambia el nombre de usuario.
- **-L:** Bloquea la cuenta para que el usuario no pueda registrarse.