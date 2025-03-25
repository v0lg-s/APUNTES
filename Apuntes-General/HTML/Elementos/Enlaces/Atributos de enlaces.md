- *href:* Permite incluir el enlace o la ruta a la que se debe redirigir al hacer clic.
- *title:* El atributo title da una previsualización de lo que pongamos al pasar el mouse por encima, sirve con cualquier elemento. Se suele usar con imágenes, enlaces, botones y forms
- *target:* Permite especificar dónde mostrar la URL enlazada. *_blank* abre el recurso en una nueva pestaña. *_self* abre el recurso sobre la misma pestaña (Valor por defecto).

**Nota de seguridad:** Siempre que se use el atributo **`target="_blank"`** y redirijamos a un enlace externo ajeno de nuestra propiedad, es importante usar el atributo **`rel="noopener noreferrer"`**, esto evita ataques de de *tabnabbing*. 

- **noreferrer:** protege la privacidad del usuario, evita que la página enlazada reciba información sobre la página de origen (referer).
	- Al usar `noreferrer`, el servidor del sitio enlazado no puede ver desde qué página provino el tráfico.
- **noopener:** evita que la página enlazada (a la que el usuario accede) **pueda controlar o manipular la página de origen** mediante el objeto `window.opener` en JavaScript.
	- La página maliciosa ya **no puede modificar** o **redirigir** la página original.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Enlaces 2</title>
    </head>  

    <body>
        <h1>Segunda pagina con enlaces</h1>
        <h2>Enlace que se abre en otra pestaña</h2>

        <! --El atributo target con valor _self indica que el recurso se abrirá sobre la misma pestaña en la que estamos actualmente (es el valor por defecto). Con valor _blank abre el recurso en una nueva pestaña.-->

        <a href="../listas.html" target="_blank" rel="noopener noreferrer">Podemos ir a Listas y abrirlo en otra pestaña</a>

        <a href="enlaces.html">Volver a enlaces 1</a>

    </body>

</html>
```