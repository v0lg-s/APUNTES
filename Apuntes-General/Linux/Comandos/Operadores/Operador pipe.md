# Operador "pipe |"
Este operador envía el standard output de un comando cómo el standard input de otro.
Es como una tubería con dos extremos.

```bash
ls -al | less 
```

Envía la salida del comando "ls -al" al comando "[[Head, Tail & less - Lectura de Archivos Grandes|less]]" que se encarga de mostrar el contenido en una pagina para que archivos grandes de texto sean más fáciles de leer.