**RIGHT JOIN** retorna todos los registros de la segunda tabla, pero solo los registros de la segunda tabla qué coincidan en una columna especificada.
![[RIGHT-JOIN.png]]
**EJEMPLO:** 
Suponiendo que tenemos una base de datos con 2 tablas:

|   Empleados    |
| :------------: |
|  id_empleado   |
|    username    |
|  departamento  |
|    oficina     |

| id_empleado |  oficina   |
| :---------: | :--------: |
|    1000     |  Este-170  |
|    1001     | Centro-276 |
|    1003     | Norte-172  |
|    1004     |   Sur-23   |

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

La tabla *Empleados* será la primer tabla o tabla de la izquierda mientras que la tabla *Dispositivos* será la tabla de la derecha o segunda tabla. Cuando hagamos un **RIGHT JOIN** entre ambas, obtendremos los registros de la tabla de *Empleados* en los que el campo *id_empleado* coinciden, y adicionalmente todos los otros registros de la tabla *Dispositivos.* 

| id_empleado |  oficina   | id_dispositivo | sistema_operativo |
| :---------: | :--------: | :------------: | :---------------: |
|    1000     |  Este-170  |  a3201sgerv12  |        OS1        |
|    1001     | Centro-276 |   ns231dfg23   |        OS1        |
|    NULL     |    NULL    |  asd234kig34   |        OS2        |
|    NULL     |    NULL    | adwf564jgjt86  |        OS1        |
