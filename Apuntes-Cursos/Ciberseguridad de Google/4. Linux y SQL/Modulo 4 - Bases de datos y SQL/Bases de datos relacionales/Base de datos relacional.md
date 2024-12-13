Es una base de datos estructurada que contiene tablas que se relacionan entre ellas.

# Tablas
Las tablas constan de columnas, que son las características de la entidad representada por la tabla. A su vez cada columna tiene filas, también conocidas como los registros, esta es la información que se le da a la base de datos para almacenar.

|    Empleado    |
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

# Llave primaria
La llave primaria es un campo irrepetible que identifica a uno y solo uno de los registros. En el caso de la tabla empleado la llave primaria es su id. No hay un empleado con más de un id, ni hay otro empleado con el mismo id que otro.

# Llave foránea
La llave foránea se utiliza para relacionar 2 tablas en una base de datos, esta llave foránea es la llave primaria de otra tabla. En la tabla Empleado es posible que el id_dispositivo se la llave primaria de una tabla llamada Dispositivo. 