Lee una variable y según su valor ejecuta una sentencia de código.

Sintaxis:


```bash
case $variable in
	valor1) comando ;;
	valor2) comando ;;
	valorN) comando ;;
	*) comando_default ;;
esac
```

**Ejemplo:**

```bash
read -p "Elige una opción (1/2): " opcion
case $opcion in
    1) echo "Elegiste la opción 1" ;;
    2) echo "Elegiste la opción 2" ;;
    *) echo "Opción no válida" ;;
esac
```
