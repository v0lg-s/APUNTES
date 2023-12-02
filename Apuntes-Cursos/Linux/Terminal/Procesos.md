# Ver los procesos corriendo en el momento

## Comando ps
Este comando nos permite ver una captura de los procesos ejecutándose en el momento en que se hizo el llamado al comando.

Es útil usar el argumento -ef para mostrar todos los procesos.

## Comando htop
Nos ofrece una interfaz gráfica de los procesos ejecutándose en el momento.

# Kill procesos
Si requerimos *"matar" un proceso* podemos usar el comando "kill" junto al identificador del proceso. Por ejemplo:

```bash
kill -9 2986 
```
-9 es una "signal" y es la señal que enviará "kill" al proceso. La señal por defecto es -15 que pide al proceso cerrarse sin forzar, por otro lado, -9 hace un cierre forzado del proceso.

Este número se encuentra en la columna izquierda al ejecutar el comando ps -e o ps -ef.

![[grepCommand.png]]

