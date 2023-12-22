# Usuario y Contraseña
El comando ssh recibe como parámetros el usuario y el host de la siguiente manera:

```bash 
ssh usuario@nombreHost
```

El comando usa por defecto el puerto 22, si necesitamos conectar al host por medio de otro puerto podemos usar -p e indicar un número de puerto distinto.

```bash
ssh usuario@nombreHost -p 2220
```