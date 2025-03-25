Se ejecuta hasta que la condición sea verdadera.

Su sintaxis:

- Inicia con la palabra reservada `until`.
- La condición va seguida de la palabra `until` y de la misma manera que con el condicional `if`, va dentro de corchetes '[ ... ]'. **La condición debe ir separada de los corchetes.** 
- Tras la condición ';' y la palabra reservada `do`.
- Para cerrar el bucle while se usa la palabra reservada `done`.

```bash
contador=1
until [ $contador -gt 5 ]; do
    echo "Contador: $contador"
    contador=$((contador + 1))
done
```
