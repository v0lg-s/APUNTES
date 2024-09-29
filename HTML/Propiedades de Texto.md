- *Fuente:* Se pueden poner varias opciones de fuentes en caso de que la primera no cargue.
```css
p{
font-family: times,arial,sans-serif;
}
```
- *Tamaño de letra:* Tamaño de letra en pixeles, hay diferentes unidades de medida.
```css
p{
font-size: 25px;
}
```
- *Grosor de la letra:* Los números del 100 al 900 definen el grosor sin embargo algunas fuentes no definen algunos rangos. Bold = 700
```css
p{
font-weight: 500;
}
```
- *Estilo de la fuente:* Estilo de la fuente, puede ser itálica u oblicua.
```css
p{
font-style: italic;
}
```
- *Alineación del texto:* Alinea el texto de acuerdo al contenedor, se puede justificar, alinear a la derecha, izquierda o centro. Siempre es relativo a su sección contenedora.
```css
p{
text-align: justify;
}
```
- *Interlineado:* Espacio entre las líneas de texto.
```css
p{
line-height:2cm;
}
```
- *Espacio entre letras:* Define el espacio entre las letras de una misma palabra.
```css
p{
letter-spacing:1cm;
}
```
- *Transformaciones de texto:* Podemos realizar modificaciones al texto mediante esta propiedad, capitalize pone en mayúscula la primer letra de cada palabra, uppercase pone todas las letras en mayúscula.
```css
p{
text-transform: capitalize;
}
```
- *Decoraciones al texto:* Se pueden hacer modificaciones al texto como subrayado, tachado, etc.
```css
p{
text-decoration:line-through;
}
```