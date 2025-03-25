## Comando uniq
El comando uniq reporta u omite líneas repetidas en un archivo.

Tiene varias opciones útiles:
- **-c:** Esta opción muestra un prefijo a cada línea con el número de ocurrencias.
- **-d:** Esta opción hace que solo se muestren las líneas repetidas en la salida.
- **-u:** Esta opción solo muestra las líneas únicas.

```bash
uniq -u data.txt
```

Tener en cuenta que el archivo debe estar ordenado, de otra manera, uniq no funcionará.

Es útil hacerlo con [[sort - Comando]].

```bash
sort data.txt | uniq -u
```

No detecta líneas repetidas a menos que sean adyacentes. Lo dice el manual.