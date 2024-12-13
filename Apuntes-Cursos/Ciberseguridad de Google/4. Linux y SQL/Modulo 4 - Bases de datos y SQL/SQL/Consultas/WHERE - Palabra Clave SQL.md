**WHERE** es una palabra clave usada para filtrar con una o más condiciones dadas.
Las condiciones de la clausula **WHERE** van acompañadas de operadores.

```SQL
SELECT firstname, lastname, title, email
FROM employees
WHERE title = 'IT Staff';
```

Solo los empleados con el titulo de "IT Staff" van a aparecer en los registros.

# Filtrado por patrones
- Se puede filtrar por entradas que empiezan o terminan con un carácter o caracteres determinados. Para esto se deben añadir dos elementos adicionales a parte de **WHERE** a la consulta.
	- Un comodín
	- El operador **LIKE**

## Comodines
Un **comodín** es un carácter especial que puede ser sustituido por cualquier otro carácter. Dos de los comodines más útiles son el signo de porcentaje (%) y el guion bajo ( _ ):
- El % sustituye cualquier otro carácter.
- El guion bajo solo sustituye a otro carácter.

| **Patrón** | **Resultados que podría devolver** |
| :--------: | :--------------------------------: |
|    'a%'    |          apple123, art, a          |
|    'a_'    |             as, an, a7             |
|   'a__'    |           ant, add, a1c            |
|    '%a'    |           pizza, Z6ra, a           |
|    '_a'    |             ma, 1a, Ha             |
|   '%a%'    |           Again, back, a           |
|   '_a_'    |           Car, ban, ea7            |

## Operador LIKE
**LIKE** se utiliza con **WHERE** para buscar un patrón en una columna.

**Por ejemplo**, si desea enviar un correo electrónico a los empleados cuyo título sea 'IT Staff' o 'IT Manager', puede utilizar el operador LIKE combinado con el comodín %:

```SQL
SELECT lastname, firstname, title, email
FROM employees
WHERE title LIKE 'IT%';
```

**Como otro ejemplo**, si desea buscar en la tabla de facturas para encontrar todos los clientes ubicados en estados con una abreviatura de 'NY', 'NV', 'NS' o 'NT', puede utilizar el patrón 'N_' en la columna state:

```SQL
SELECT firstname,lastname, state, country
FROM customers
WHERE state LIKE 'N_';
```
