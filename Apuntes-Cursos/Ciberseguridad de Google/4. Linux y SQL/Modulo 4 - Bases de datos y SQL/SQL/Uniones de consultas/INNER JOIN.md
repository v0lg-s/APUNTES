Un **INNER JOIN** devuelve las filas que comparten un valor en una columna que existe en más de una tabla.
![[INNER-JOIN.png]]
**Ejemplo:**
Suponiendo que tenemos una base de datos con 2 tablas:

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
|    1003     |      NULL      |  mlukas  |   Finances   | Norte-172  |

|   Dispositivos    |
| :---------------: |
|  id_dispositivo   |
|    id_empleado    |
| sistema_operativo |

| id_dispositivo | id_empleado | sistema_operativo |
| :------------: | :---------: | :---------------: |
|  a3201sgerv12  |    1000     |        OS1        |
|   ns231dfg23   |    1001     |        OS1        |
|  asd234kig34   |    NULL     |        OS2        |
| adwf564jgjt86  |    NULL     |        OS1        |

Queremos ejecutar una consulta en la que obtengamos una lista de empleados, su oficina de localización y además qué sistema operativo usan en sus dispositivos.  
Para esto se debe efectuar un *INNER JOIN* para que la columna *id_empleado* de ambas tablas coincida.

```SQL
SELECT username, oficina, sistema_operativo
FROM empleados
INNER JOIN dispositivos ON empleados.id_empleado = dispositivos.id_empleado;
```

El resultado será algo cómo:

| username |  oficina   | sistema_operativo |
| :------: | :--------: | :---------------: |
| Elarson  |  Este-170  |        OS1        |
| bmoreno  | Centro-276 |        OS1        |

