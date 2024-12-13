Los módulos de python son archivos que contienen funciones adicionales, variables, clases y cualquier tipo de código ejecutable. Pueden ir desde simples y pocas líneas de código hasta ser complejas y extensas.

# Módulos de la librería estándar de Python
## Modulo re
Modulo útil para analistas cuando tienen tareas de búsqueda de patrones en archivos de registro.

## Modulo csv
Permite trabajar eficientemente con archivos csv.

## Módulos glob y os
Para interactuar con la línea de comandos.

## Módulos time y datetime
Permite trabajar con marcas de tiempo y fecha.

## Módulo statistics
El módulo statistics incluye funciones utilizadas al calcular estadísticas relacionadas con datos numéricos. Por ejemplo, mean() es una función del módulo statistics que toma datos numéricos como entrada y calcula su media (o promedio). Además, median() es una función del módulo statistics que toma datos numéricos como entrada y calcula su mediana (o valor medio).

# ¿Cómo se importan? 

## Librería estandar
Cuando se trata de un modulo de la librería estándar de Python, se usa:

```Python
import statistics
```

Con lo anterior se importa todo el módulo, es decir, todas las funciones contenidas en el módulo. 
Por lo que al usar una función de este módulo debemos hacer el llamado indicando el nombre del modulo seguido de un punto y posteriormente el nombre de la función.

```Python
import statistics
statistics.median(1,2,3,4,5,6,7,8)
```

Cuando deseamos una función específica de un modulo se usa:

```Python
from statistics import median
```

El llamado a esta función será más simple:

```Python
from statistics import median, mean
median(1,2,3,4,5,6,7,8)
mean(23,34,45,54,65,56)
```

## Librerías externas
Cuando importamos modulos de librerías externas, se usa:

1. Se debe instalar la librería desde la línea de comandos: `pip install numpy`
2. Una vez descargada se puede importar.

```Python
import numpy
```