Son usados para recoger información procesable desde la página. Se utiliza la etiqueta **`<form>`** e **`<input>`**. Si ponemos un input fuera de **`<form>`** ese input no tendrá valor en el procesamiento de datos.

```html
<!DOCTYPE html>

<html lang="es">
    <head>
        <title>Formularios</title>
    </head>

    <body>
        <form>
            <h2>campo texto</h2>
            <input type="text" placeholder="Introducir Nombre">
            
            <h2>Boton de enviar</h2>
            <input type="submit" value="Texto del boton de enviar">

            <h2>campo en formato email</h2>
            <input type="email" placeholder="xxxxxx@gmail.com">

            <h2>campo contraseñas</h2>
            <input type="password" required minlength="5" name="contraseña">

            <h2>check</h2>
            <input type="radio">

            <h2>campo para archivo</h2>
            <input type="file">
        </form>

    </body>

</html>
```



