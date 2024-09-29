También son llamados hipervínculos, nos llevan a recursos dentro o fuera del sitio web.

La etiqueta para describir un enlace es:
```html
<a href="https://youtube.com">Enlace a youtube</a>
```
**EJEMPLO:**

```html
<!DOCTYPE html>
<html>
	<head>
		<title>ENLACES</title>
	</head>

	<body>
        <h1>PAGINA CON ENLACES</h1>
        <h2>Enlace externo</h2>
        
        <a href="https://facebook.com">Ir a Facebook mano.</a>
        
        <h2>Enlace local con titulo al pasar el mouse</h2>
        <! --Hay que tener en cuenta que para redirigir a un recurso local omitimos el https-- >

        <a href="enlaces_2.html" title="Este enlace te lleva a otra pagina gg">Ir a enlaces 2 bro</a>
	</body>
</html>
```

## Atributos
- *href:* Permite incluir el enlace o la ruta a la que se debe redirigir al hacer clic.
- *title:* El atributo title da una previsualización de lo que pongamos al pasar el mouse por encima, sirve con cualquier elemento. Se suele usar con imágenes, enlaces, botones y forms
- *target:* Permite especificar dónde mostrar la URL enlazada.

```html
<!DOCTYPE html>

<html>

    <head>

        <title>Enlaces 2</title>

    </head>

  

    <body>

        <h1>Segunda pagina con enlaces</h1>

        <h2>Enlace que se abre en otra pestaña</h2>

        <!--El atributo target con valor _self indica que el recurso se abrirá sobre la misma pestaña en la que estamos actualmente (es el valor por defecto). Con valor _blank abre el recurso en una nueva pestaña.-->

        <a href="../listas.html" target="_blank">Podemos ir a Listas y abrirlo en otra pestaña</a>

        <a href="enlaces.html">Volver a enlaces 1</a>

    </body>

</html>
```