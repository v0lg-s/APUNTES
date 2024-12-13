Es un operador que nos permite filtrar dentro de un intervalo o rango.

**Ejemplo:**

```SQL
SELECT *
FROM machines
WHERE OS_patch_date BETWEEN '2021-03-01' AND '2021-09-01';
```

En este ejemplo usamos **BETWEEN** para filtrar las fechas de parche de actualización realizadas entre dos fechas.