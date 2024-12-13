Podemos usar la palabra clave **ORDER BY** en una consulta para organizar los datos que extrae de una tabla.

# Ordenar ascendentemente
Se escribe al final de la consulta y se especifica una columna en la que basar la ordenación.

```SQL
SELECT customerid, city, country
FROM customers
ORDER BY city;
```

![[consultaORDER-BY.png]]

**Nota:** Si se elige una columna con datos numéricos se ordenarán de menor a mayor.
Si se elige una columna con caracteres alfabéticos se ordenarán en orden alfabético.
# Ordenar descendentemente
Para ordenar en descenso se usa la palbra clave **DESC** después de **ORDER BY**.

```SQL
SELECT customerid, city, country
FROM customers
ORDER BY city DESC;
```

# Ordenar basado en varias columnas
Se pueden elegir varias columnas para ordenar los registros.
- **Por ejemplo**, puede elegir primero la columna ``country`` y después la columna ``city``. A continuación, SQL ordena la salida por ``country``, y para las filas con el mismo country, las ordena basándose en ``city``.

```SQL
SELECT customerid, city, country
FROM customers
ORDER BY country, city;
```

