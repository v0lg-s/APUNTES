# Locales
Las variables locales solo existen dentro del script o función determinada.

# Globales
Son variables disponibles en otros scripts y procesos. Se definen usando `export`.
```bash
export nombre="Juan"
```
# De solo lectura
Son variables que solo pueden ser leídas y su valor no puede ser modificado. Se definen usando la palabra clave `readonly`.

```bash
readonly constante="valor"
```

# Especiales

| **Variable** |                         **Descripción**                         |
| :----------: | :-------------------------------------------------------------: |
|     `$0`     |                        Nombre del script                        |
| `$1, $2...`  |                      Argumentos del script                      |
|     `$#`     |                 Número de argumentos recibidos                  |
|     `$@`     |                      Todos los argumentos                       |
|     `$?`     | Estado del último comando (0 si fue exitoso, 1 de lo contrario) |
|     `$$`     |                    ID del proceso del script                    |
