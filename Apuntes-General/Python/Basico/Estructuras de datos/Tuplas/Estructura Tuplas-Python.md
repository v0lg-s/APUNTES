Es un tipo de dato en python que permite almacenar una secuencia de datos ordenados, sin importar su tipo, es decir, una lista puede almacenar desde datos de tipo **`int`** **`float`**.

**Características:**
- **Ordenadas:** La posición dentro de la estructura importa. (Maneja indices)
- **Heterogéneas:** Almacenan distintos tipos de datos.
- **Inmutables:** NO se pueden modificar una vez creadas.

*Sintaxis:*

```python
#Tuplas
tupla1 = (29, True, "Cadena de texto", 3.1416)
tupla2 = 1.0, 0.5, 0.25, 0.125
tupla_de_un_elemento = (1, )
```

Todas son tuplas, se pueden definir sin uso del paréntesis.

**Indices**
Para acceder a cada uno de sus elementos podemos usar la posición de cada elemento. Dentro de corchetes al igual que en las listas

```python
print(tupla[0]) #para el primer elemento
```

