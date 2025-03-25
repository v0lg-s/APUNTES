## Comando grep
Muestra las líneas que coinciden con un patrón dado. Podemos usar el operador [[Desarrollo Fotogrametría#Operador "pipe "|pipe]] para redirigir salidas de comandos y filtrar.

Un ejemplo muy útil es para filtrar procesos en la lista de tareas activas. Usando el comando [[Procesos#Comando ps|ps -ef]]

```bash
ps -ef | grep brave
```

De esta manera obtendremos los procesos que está corriendo la aplicación brave.

![[grepCommand.png]]
