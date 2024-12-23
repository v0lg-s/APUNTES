# Usuario y Contraseña
El comando ssh recibe como parámetros el usuario y el host de la siguiente manera:

```bash 
ssh usuario@nombreHost
```

El comando usa por defecto el puerto 22, si necesitamos conectar al host por medio de otro puerto podemos usar -p e indicar un número de puerto distinto.

```bash
ssh usuario@nombreHost -p 2220
```

Usando la opción **-i** indicamos que vamos a pasar un archivo que contiene una llave privada, para acceder al host remoto.

```bash
ssh usuario@direccionHost -p 2220 -i ./rsa_id
```

Esta es una alternativa al acceso con contraseña.

- **Copiar archivos con SCP (Secure Copy Protocol):**
```bash
scp archivo.txt usuario@direccion_ip:/ruta/destino
```
    
- **Copiar archivos con SFTP (Secure File Transfer Protocol):**
```bash
sftp usuario@direccion_ip 
```
    
- **Túnel SSH:**
```bash
ssh -L puerto_local:localhost:puerto_remoto usuario@direccion_ip 
```
