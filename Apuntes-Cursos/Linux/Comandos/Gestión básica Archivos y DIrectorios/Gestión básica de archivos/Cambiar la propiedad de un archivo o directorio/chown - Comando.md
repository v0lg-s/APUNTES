El comando **chown** cambia la propiedad de un archivo o directorio. 
- Se puede utilizar chown para cambiar la propiedad del usuario o del grupo. 
- Para cambiar el usuario propietario del archivo access.txt a fgarcia:
```bash
sudo chown fgarcia access.txt
```

- Para cambiar el propietario de grupo de access.txt a security:
```bash
sudo chown :security access.txt
``` 
Se deben introducir dos puntos (:) antes de security para designarlo como nombre de grupo.