Modelo que describe como se deberían poner los elementos de HTML en una pagina web.  
Define los tamaños, formas e interacciones entre estos elementos.

- Se entiende que cada elemento que definimos en un documento HTML se muestra en el navegador en forma de caja rectangular, no existen elementos circulares, triangulares ni poligonales.
- Con CSS podemos cambiar las propiedades de estas cajas como el tamaño, el color, los estilos, la margen y más.

# Áreas del Box Model

![[css-box-model.png]]
## Content / Contenido
El área del content (como su nombre lo dice) contiene el “contenido” central a mostrar, es decir, un texto, una imagen, un video, etc. El contenido siempre es *lo que queremos mostrarle al usuario*. Esta área en muchas ocasiones tiene un color o imagen de fondo para hacerla más atractiva.
### Propiedades
- **Height:** Altura.
- **Width:** Ancho.
- **max-height**
- **max-width**
- **min-height**
- **min-width**
## Padding / Relleno
Espacio entre el contenido y el borde el elemento. No tiene color, simplemente separa el contenido del borde.
- El padding sigue siendo parte de la caja visible, por lo que, si tenemos una imagen o color de fondo, este se extenderá a través del padding. El padding está delimitado por el borde.
### Propiedades
- **Padding:** Podemos cambiar esta distancia de manera uniforme hacia todos los lados con:
```css
padding: 20px;
```
- **Padding-(lado):** Podemos cambiar la distancia especificando el lado en inglés:
```css
padding-left:10px;
padding-right:15px;
/*Esto solo modifica el padding hacia el lado izquierdo y derecho.*/
```

Podemos hacer lo mismo en una sola línea si queremos modificar el padding en todos los sentidos o solo algunos.

```css
padding: 10px 20px 25px 5px; /*top | right | bottom | left*/
padding: 10px 20px; /*vertical | horizontal*/
```

## Border /Borde
Rodea el contenido y al padding.
Tiene propiedades modificables como el color, el estilo y el grosor.
### Propiedades
- **Border-Style:** Estilo de la línea del borde. (Punteada, continua o entrecortada)
![[border-styles-css.png|300]]

```css
border-style: dashed;
```

- **Border-Width:** Indica al navegador el tamaño del borde. Valor en pixeles.
```css
border-width: 5px;
```

- **Border-Color:** Cambia el color del borde.
- **Border-radius**: Cambia el estilo de las esquinas.
```css
p{
border-radius: 20px;
}
```
## Margin / Margen
Es la separación entre una caja y las cajas adyacentes.

El margen es la última área del Box Model y se puede ver como una separación invisible o transparente que ayuda a separar un elemento de otro. Cuando definimos un color o imagen de fondo, este no se propaga a esta sección.
### Propiedades
- **Margin:** Podemos cambiar esta distancia de manera uniforme hacia todos los lados con:
```css
margin: 20px;
```
- **Margin-(lado):** Podemos cambiar la distancia especificando el lado en inglés:
```css
margin-left:10px;
margin-right:15px;
/*Esto solo modifica el margin hacia el lado izquierdo y derecho.*/
```

Podemos hacer lo mismo en una sola línea si queremos modificar el margin en todos los sentidos o solo algunos.

```css
margin: 10px 20px 25px 5px; /*top | right | bottom | left*/
margin: 10px 20px; /*vertical | horizontal*/
```
