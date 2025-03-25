 La estructura de una página web básica es la siguiente:

![[estructuraHtml.png]]

# Etiqueta **<!DOCTYPE html>** 
```html
<!DOCTYPE html>
```

Esta primera línea de código indica la versión de HTML que usaremos a lo largo del código.

# Etiqueta raíz
```html
<!DOCTYPE html>
<html>

</html>
```

La etiqueta HTML es la raíz de todo documento HTML.

A esta etiqueta podemos darle atributos como el lenguaje de todo el documento HTML, serán metadatos.
## Etiqueta Head
La pagina web se compone de dos etiquetas.
1. En primer lugar *"head"* contendrá información propia de la página como el titulo y algunos metadatos.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<title>Titulo de la página web</title>	
	</head>
</html>
```

## Etiqueta Body
2. En segundo lugar tenemos la etiqueta *"body"* contendrá toda la parte visual de la página web. Representa todo el contenido del documento HTML.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<title>Titulo de la página web</title>	
	</head>
	<body>
	TODO EL CONTENIDO DE LA PAGINA IRÁ AQUÍ
	</body>
</html>
```