Una consulta básica en SQL consta de 2 palabras clave, **SELECT** y **FROM**.

**SELECT:** Indica qué columnas queremos consultar de una tabla especificada en...
**FROM:** Indica de qué tabla queremos consultar.

**Nota:** El asterisco * significa todo/todas.

**Ejemplo:** Con la tabla de Empleados: 

|   Empleados    |
| :------------: |
|  id_empleado   |
| id_dispositivo |
|    username    |
|  departamento  |
|    oficina     |


| id_empleado | id_dispositivo | username | departamento |  oficina   |
| :---------: | :------------: | :------: | :----------: | :--------: |
|    1000     |  a3201sgerv12  | Elarson  |  Marketing   |  Este-170  |
|    1001     |   ns231dfg23   | bmoreno  |  Marketing   | Centro-276 |
|     ...     |      ...       |   ...    |     ...      |    ...     |

Queremos ver los empleados y el dispositivo que usa, para esto la siguiente consulta nos puede ayudar:

```SQL
SELECT id_empleado, id_dispositivo FROM Empleados;
```

El resultado sería:

| id_empleado | id_dispositivo |
| :---------: | :------------: |
|    1000     |  a3201sgerv12  |
|    1001     |   ns231dfg23   |
|     ...     |      ...       |

