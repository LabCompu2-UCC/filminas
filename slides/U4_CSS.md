---
title: CSS
theme: black
slideNumber: true
---

# CSS
<small>
Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88") & 
<i class="fab fa-telegram"></i>
[rmarku]("https://t.me/rmarku")
</small>

---
## CCS: Cascading Style Sheets
Hojas de Estilo en Cascada (CSS) es un lenguaje de estilo de hojas usado para describir la presentación de las páginas web escrito en HTML o XML.

CSS permite la separación del contenido del documento de la presentación del documento (disposición, colores, fuentes, etcétera).

---
## Capas del Diseño Web
![Capas](images/html/capas.png)

---
## CCS3: Cascading Style Sheets
Estilos visual del documento.
* Selectores
* Modelos de Caja
* Fondos y Bordes
* Valores de imagenes y Remplazo de contenido
* Efectos de texto
* Transformaciones 2D/3D
* Animaciones
* Multiples columnas
* Interfaz de Usuario

---
![CSS3 Historia](images/html/CSS3_historia.png)

---
## CSS: Sintaxis
![CSS Sintaxis](images/html/css-sintaxis.png)

---
## Formar de Agregar Estilos
* Estilo en Linea
* Incrustando una Hoja de Estilo
* Enlazando una hoja de Estilo Externa

---
## Estilo en Linea
* Se usa el atributo "style" para definir como la etiqueta debe mostrarse.
* Ejemplo:
````html
<h1 style="color: red; font-type: helvetica; font-size: 2em">
````
---
## Hoja de Estilo Incrustada
* Se incorpora en &lt;head&gt;
*  Se describe:
````html
<style>
   Selector{
propiedad: valor;
   }
</style>
````
Ejemplo:
````html
h1{
color: #333333;
font-weight: bold;
margin-left: 15px;
}
````
---
## Propiedades tipográficas
* **font-family:** se define tipografía por orden de prioridad
* **font-size:** Se define tamaño
* **font-style:** italic, normal
* **font-weight:** bold, normal, ultrabold, o números 100,200,300
* **color:** nombre, hexadecimal, rgb
* **letter-spacing:** interletrado
* **world-spacing:** espacio entre palabras
* **line-height:** tamaño del renglon (altura de línea)
* **text-align:** right, left, center
* **text-decoration:** underline, line-through, none
* **text-indent:** sangria
* **text-transform:** uppercase, lowercase

---
## Colores
* Por nombre: <h1 style="color: red>

* Hexadecimal: <h1 style="color: #CA98E3>
[Colores Hexadecimales](http://html-color-codes.info/codigos-de-colores-hexadecimales)

* RGB: <h1 style="color: rgb(205, 92, 92)>

---
## Ejercicio: Propiedades tipográficas
Escribe un código con la siguiente estructura:

````html
<p>Este es el primer párrafo
<h1>Titulo 2</h1>
<p>Este es el SeGuNdO PáRRaFo
````

---
## Empleando estilo en línea
* Utilice **font-family**, **font-size** y **font-style** para el primer titulo
* Utilice **font-weight**, **text-decoration** y **color** para el segundo titulo
* Emplee **letter-spacing**, **line-height** y **text-align** para el primer párrafo
* Emplee **world-spacing**, **text-indent** y **text-transform** para el segundo párrafo
* underline, line-through, none

---
##  ¿Como Escribir un Estilo? 
Obviamente, con el teclado xD. Bue, hablando en serio, hay 3 formas:

1. **por Tag** (se aplica a TODOS los selectores)
````html
selector{nombreEstilo: valor;}
````

2. **por ID** (para identificar elementos unívocos)
````html
#nombreID {nombreEstilo: valor;}
````

3. **por Clase**
````html
.nombreClass {nombreEstilo: valor;}
````

---
## Ejercicio: Selectores
Escribe un código con la siguiente estructura:
````html
<h1 id="principal">Titulo 1</h1>
<p>Este es el primer párrafo
<h1 class="mi-titulo">Titulo 2</h1>
<p>Este es el SeGuNdO PáRRaFo</p>
````
Empleando una hoja de estilo incrustada
* A todas las etiquetas &lt;p&gt; aplicar el mismo tipo de tipografía y color.
* Para el titulo **#principal** emplear un font-size
* A la clase **.mi-titulo** emplee un text-decortation

---
##  Descendientes
* **selectores:** 
````css
ul li{nombreEstilo: valor;}
````

* **de ID:** 
````css
#nombreID h1{nombreEstilo: valor;}
````

* **de Clase:**
````css
.nombreClass p{nombreEstilo: valor;}
````
---
## Ejercicio: Estilo con Descendientes
* Cree 2 listas no ordenadas y agregue estilos para visualizarla con círculos y con cuadrados.
* Cree 2 listas ordenadas y agregue estilos para visualizarla con números romanos y letras griegas.
   
---
## Pseudo Clases
````css
/* unvisited link */
a:link {
   color: #FF0000;
}

/* visited link */
a:visited {
   color: #00FF00;
}

/* mouse over link */
a:hover {
   color: #FF00FF;
}

/* selected link */
a:active {
   color: #0000FF;
}
````

---
## Ejercicio: Pseudo Clases
Cree un hipervinculo en una pagina
Empleando Pseudo clases:
* Link visitado o no visitado con el mismo color
* Al posicionar el mouse arriba del link, modificar el tamano de la fuente
* Al seleccionar el link, seleccionar BOLD

---
## CCS3
Buenas Practicas:
* Comprobar el diseño en varios navegadores
* Depuracion (Ej. firebug)
* Comentar el código
* Identar y hacer el código fácil de leer
* Usar sistema comun de nombrado
* Evitar tamaños absolutos en fuentes o elementos
* Utilizar notación de colores en hexadecimal
* Ordenar los elementos según pertenezcan a cabecera, contenido principal o pie de página

---
## Modelo de Cajas
![Padding y Margin](images/html/pading_margin.gif)

---
##  Alto y Ancho 
````css
div{
   width: 80%;
   height: 100px;
}
````
unidad de medida | porcentaje | auto | inherit (hereda del padre)

---
##  Unidades de Medida 
Las unidades relativas disponibles son:
* **em:** el tamaño de fuente del elemento contenedor
* **ex:** la altura de la letra x de la fuente del elemento contenedor
* **ch:** la altura de la cifra 0 (cero) de la fuente del elemento contenedor
* **rem:** el tamaño de la fuente del elemento raíz de la página
* **vw:** % del ancho visible
* **vh:** % del alto visible
* **vmin:** % del valor menor entre ancho y alto visible
* **vmax:** % del valor mayor entre ancho y alto visible

### En la práctica, las unidades relativas más utilizadas son em y rem, y vw y vh.

---
Las unidades absolutas disponibles son:
* **px:** píxeles
* **cm:** centímetros
* **mm:** milímetros
* **q:** cuartos de milímetros
* **in:** pulgadas (1in = 2.54cm = 25.4mm)
* **pc:** picas, la sexta parte de una pulgada
* **pt:** puntos, la doceava parte de una pica

---
##  Margin & Padding 
1. Establecerlos por separado
````css
div{
   margin-top: 15px;
   margin-right: 20px;
   margin-bottom: 10px;
   margin-left: 5px;
   }
````
2. Establecer top-bottom & right-left:
````css
div{margin: 15px 20px;}
````
3. Establecer todo junto:
````css
div{margin: 15px 20px 10px 5px;}
````

4. Margenes iguales:
````css
div{margin: 15px;}
````

5. Establecer top, right/left, bottom:
````css
div{margin: 15px 20px 5px;}
````

---
##  Borde 
* .estilo-borde {border: grosor tipo color}
````css
.estilo-borde{2px solid blue;}
/*dotted, dashed, solid, double, groove, ridge, inset, outset*/
````

---
<!-- .slide: data-background="linear-gradient(to right, red , yellow)" -->
## Fondo y Gradientes
````css
/* solo color */
background: red;
/* gradiente */
background: linear-gradient(to right, red , yellow);
/* imagen de fondo */
background: url("fondo.png");
````

---
## Comentario
````css
/* Este es un
comentario CSS de varias
lineas */
````

---
## Ejercicio: Modelo de Cajas
Cree 4 divs
* Asigne diferentes colores para cada uno
* Modifique el Padding o margen interno
* Modifique el Borde de cada caja
* Modifique el Margen de cada caja
* Agregue comentarios a los estilos

---
## Ejercicio: CV
Diseñe un CV y agregue estilos empleando una hoja de estilo incrustada:
* Emplear &lt;div&gt; para la estructura de la página. Agregue atributos de margin y padding.
* Agregar una imagen en el primer &lt;div&gt; y alinee a la izquierda
* Emplear &lt;h1&gt; para el nombre y &lt;h2&gt; para la ocupación
* Dentro de los &lt;div&gt;, utilizar &lt;h3&gt; para cada título y &lt;p&gt; para la descripción
* Centrar todo el contenido del body.
* Agregar <a href="https://fonts.google.com/" target="_blank"> fuentes de google </a> para personalizar la página
* Agregar background al body, que posea <a href="https://www.w3schools.com/csS/css3_gradients.asp" target="_blank">gradiente</a>
* Redondear las esquinas de la imagen para dejarla circular. Redondear las esquinas de los &lt;div&gt; y elegir un color y un estilo
* Cambiar el favicon

---
## Ejercicio: CV
![CV Imagen](images/html/cv_imagen.png)

---
## Position
Como posicionar elementos dentro de la pagina.
* static
* relative
* fixed
* absolute
* inherit

[W3School](https://www.w3schools.com/cssref/pr_class_position.asp)

[Learns Layout](http://es.learnlayout.com/position.html)

---
## Position: static;
Los elementos posicionados con "Static" no son afectados por las propiedades top, bottom, left y right.

Por defecto, todos los elementos HTML son Static.

---
## Position: relative;
El elemento es posicionado relativo respecto a su posición normal.
Los valores top, left, right, bottom lo mueven respecto a su posición original
Permite que un elemento se desplace respecto a lo que hubiera sido su posición normal; el resto de elementos continúan en su posición ignorando al que se desplaza, lo que puede crear superposiciones; el espacio libre que deja el elemento queda libre.

---
## Position: fixed;
El elemento "fixed" es posicionado respecto al area visible.
Los valores top, left, right, bottom lo mueven respecto a su posición original
Permite que un elemento se desplace respecto al origen de coordenadas del primer elemento contenedor posicionado ó respecto a la esquina superior izquierda de la ventana de visualización; el resto de elementos actúan como si el desplazado no existiera, por lo que su espacio será ocupado por otros elementos; puede crear superposiciones.

---
## position: absoluto;
Los elementos con position: absolute; son posicionados mediante top, left... respecto a su ancestro mas secano que este posicionado.
Un elemento posicionado es aquel que tenga en su propiedad position algo distinto a static

Permite fijar un elemento en una posición respecto al origen de coordenadas del primer elemento contenedor posicionado ó respecto a la esquina superior de la ventana de visualización; el elemento se mantendrá en la ventana de visualización o viewport, siempre en una misma posición aunque el usuario se desplace por la web haciendo scroll.

---
## position: inherit;
Se heredan las características del elemento padre.

---
## superposición con z-index
La propiedad z-index indica que elemento va estar posicionado sobre otro elemento.
Los elementos con z-index mayor tapan a los elementos con z-index menor 

---
## Float
Float se usa para envolver imágenes con texto.

[Learns Layout](http://es.learnlayout.com/float.html)

---
## Clear
para controlar el comportamiento de los floats.

[Learns Layout](http://es.learnlayout.com/clear.html)

---
## Ejercicio: 2 Columnas
Emplear <div> con style para lograr que el estilo del texto quede en 2 columnas fluidas.
* En la clase **WRAP**, emplear overflow para indicar al navegador qué es lo que debe hacer con el contenido que no cabe dentro de una capa, según las dimensiones que se le han asignado. (visible, hidden, scroll,auto)
* En la clase **SIDEBAR**, se determinara el ancho en px y el float izq (para posicionar los elementos de forma flotante)
* En la clase **MAIN**, se determinara el margin izq del tamaño del SIDEBAR o mayor para que se coloque a la derecha del sidebar.

---
## Ejercicio: 2 Columnas
![2 Columnas](images/html/2columnas.png)

---
## Hoja de Estilo Externa
* En el &lt;head&gt; se emplea un link a un archivo externo
````css
<link rel="stylesheet" href="estilos.css" type="text/css">
````
---
## Ejercicio: Hoja de Estilo Externa
Modifique la página web del CV para que los estilos incrustados estén en un archivo de estilos.
Asegúrese de por lo menos incluir un estilo por Tag, por ID y por clase.

---
## Media Queries
"Responsive Design" es la estrategia para hacer que un sitio se adapte al navegador y dispositivo en el que se muestra
````css
@media screen and (min-width:600px) {
    nav {
        float: left;
        width: 25%;
    }
    section {
        margin-left: 25%;
    }
}
@media screen and (max-width:599px) {
    nav li {
        display: inline;
    }
}
````
[Learn Layout](http://es.learnlayout.com/media-queries.html)

---
## Grid
[W3School Grid](https://www.w3schools.com/css/css_grid.asp)

---
## CSS
¿Porque una Web no funciona igual en diferentes navegadores?
<ul>
<li style="list-style-image: url('images/html/chrome.png');">
** Google Chrome **
Utiliza para interpretar JavaScript un motor **V8**, y para el renderizado **WebKit**.

<li style="list-style-image: url('images/html/firefox.png');">
**Firefox **
Emplea **JagerMonkey ** para JavaScript y para el renderizado **Gecko **.

<li style="list-style-image: url('images/html/explorer.png');">
**Internet Explore**
Emplea **Chakra** para JavaScript y **Trident** para renderizado.
</ul>

---
![Prueba Navegadores](images/html/prueba_navegadores.jpg)

---
##  CSS: Recomendación 
Revisar documentación:
[W3 School](http://www.w3schools.com/css/default.asp)

Autogenerar algunos estilos complicados:
http://css3generator.com/
http://www.css3.me/
http://westciv.com/tools/shadows/

Escribir los colores en hexadecimal:

http://html-color-codes.info/codigos-de-colores-hexadecimales/

---
## Ejemplo CCS3
<iframe width="1200" height="500" src="ejemplos/css/index2.html"></iframe>

---
## Ejemplo CCS3
<iframe width="1200" height="500" src="ejemplos/css/index.html"></iframe>

---
## Transitions
````css
div {
   width: 100px;
   height: 100px;
   background: red;
   -webkit-transition: width 2s; /* For Safari 3.1 to 6.0 */
   transition: width 2s;
}
   
div:hover {
   width: 300px;
}
````
<div class="divTran"></div>

---
## Transitions 2
````css
div {
   width: 100px;
   height: 100px;
   background: red;
   -webkit-transition: width 2s, height 2s, -webkit-transform 2s; /* Safari */
   transition: width 2s, height 2s, transform 2s;
}
   
div:hover {
   width: 200px;
   height: 200px;
   -webkit-transform: rotate(180deg); /* Safari */
   transform: rotate(180deg);
}
````
<div class="divTran2"></div>

---
## FavIcon
````css
<link rel="shortcut icon" href="/favicon.ico">
````

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)