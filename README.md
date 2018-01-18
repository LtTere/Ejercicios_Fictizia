# CÓMO FUNCIONA UN NAVEGADOR

El ordenador lee tres idiomas, **HTML,CSS y JAVASCRIPT**.

Se descarga en el caché una copia de la web en tu ordenador(CLIENT SIDE) a través de un dominio. Estos están en servidores (SERVER SIDE), con una dirección IP(números) en lugar del nombre que interpreta primero el DNS(DOMAIN NAMES SERVER), en una carpeta alojada (HOSTING).

**CLIENT SIDE—DNS—SERVER SIDE—CLIENT SIDE**

**HTML:** Alberga contenido estructurado y semántica. **Qué es.**

**CSS:** Se preocupa cómo se ve lo que ponemos en el HTML (presentación, formato, estilos…). **Cómo se ve**.

**JAVASCRIPT**: Comportamiento de los elementos de la interfaz de la descarga de datos dinámincos asíncronos (AJAX). Interactividad, **cómo funciona.** 

La importancia del CSS: http://www.csszengarden.com/ 

# DISTRIBUCIÓN DEL PROYECTO

>## CARPETAS Y ARCHIVOS

El archivo primero será la portada que SIEMPRE ha de llamarse **Index.html**

Tanto las carpetas como archivos, se eligen los nombres sin simbología, espacios, ñ, etc. El nombre del archivo es muy importante por el SEO y Google.
Ej: en lugar de poner Galeria.html poner mejor Trabajos-fotografia.html. El guión del medio siempre lo interpreta como espacio, tanto el guión bajo como el guión simple. ****Recomendación de Google** será poner el guión simple.** 

Los **HTML** no van en subcarpetas, van en raíz.

Sin embargo, el **CSS**, va en una subcarpeta en la que pondremos todo lo relacionado. El nombre de ésta carpeta no es tan importante. Ej: main.css, styles.css, css.css

Dentro de ésta, irán distintas carpetas con sus archivos según el contenido:

 - Las fotografías del CSS: son las de fondo, que va en una subcarpeta dentro del CSS. Ej: ui-img. Sus archivos serán: fondo.jpg, icono.png, icono.svg.
 - Las fuentes (fonts): Las podemos sacar de Googlefonts ó de los archivos estandars. Éstos archivos deben estar en .woof para web, si están en .ttf ó .otf deben ser convertidos. La cantidad de fuentes importa, cuantas menos mejor.

El **JS** tiene una subcarpeta con los archivos y carpetas con las librerías. Ejemplo para la carpeta de la librería: libs.

Reducimos, dentro de lo posible, al mínimo el número de carpetas y archivos por el tema del peso y cantidad de llamadas, cuanto menos mejor. 

**Las fotografías del contenido** irá en otra carpeta. Ej: img. Dentro de ésta carpeta, las fotos serán en jpg la gran mayoría y el nombre será muy importante por el tema del SEO y Google, debe ser muy descriptivo. Ej: titulo-de-la-noticia-referente.jpg .

**Los vídeos**, van en otra carpeta dentro del proyecto la cual llamaremos media si hay vídeo y audio, si sólo tenemos video la llamaremos video. El nombre del video afecta también al SEO y Google. Ej: video.mp4.  Otro archivo que hay que incluir es el poster, que es la imagen principal en jpg relacionada con el video, lo nombramos igual que el video.jpg .

**Los iconos de la web** (touch icon y los logos de la marca), éstos van sueltos sin carpeta. Los generamos de distintos tamaños a través de https://realfavicongenerator.net/ para los distintos dispositivos.

**Carpeta desastre**, ésta es la que no se sube a internet donde ponemos los PSD, los editables, los videos 4k...

![arbol](/img/arbol.png)


# HTML

Empezaremos abriendo una carpeta del proyecto, la guardamos y la vinculamos con el editor de código para comenzar con el HTML.

La primera línea de código será el Doctype que define el tipo de documento con el que vamos a trabajar, quedando así: 

				<!DOCTYPE html>

**Como anotación, toda línea de código estará escrita en minúsculas.*

La segunda línea de código, 		
			
				<html>
		Aquí va todo lo relacionado al documento.		
				</html> (para cerrar)

En tercer lugar,

	<head>
		Se utiliza para poner la información de la web como los títulos.
    </head> (para cerrar)
								 
	<title> texto </title>

 Ésta información afecta mucho al SEO y Google y también corresponde al enlace de la página. Cada página (website) lleva un title distinto obligatoriamente poniendo siempre nombres coherentes para el usuario, con información relevante en primer lugar y 60 caracteres com máximo.
                  
    <meta charset ="mapa de caracteres utf-8">
    
    <meta name = "descripcion" content = "describe el sitio"> con un máximo de 155 			   carácteres.
                  
    <meta property =" " content =" "> se utiliza en redes sociales.

En cuarto lugar,

	<body>
	Aquí se coloca todo el contenido de la web, desde la cabecera, el texto, etc.
	</body> 

Uno de los contenidos de la web son los párrafos que se representan con la etiqueta,

	<p> </p>
				  
Dentro de los párrafos, al igual que en todo el contenido de la web, es muy importante enriquecer semánticamente todo. Por ello, existen otras etiquetas que se encargan de eso dependiendo de dónde estén colocadas. En párrafo utilizamos,

	<strong> unas palabras de texto elegido </strong>
   Ésta etiqueta lleva un CSS de fábrica que pone las palabras en negrita pero posteriormente se puede cambiar en el archivo CSS.

Para cambiar la entonación, dar un énfasis distinto al texto, como por ejemplo: nombres propios, ponemos la etiqueta,

	<em> nombre propio </em>

Automáticamente se pone en cursiva, pero también lo podemos cambiar en CSS. 

Semánticamente hablando, le da un valor distinto al párrafo.

Para no cambiar la semántica de un texto pero sí darle un formato distinto posteriormente en CSS, existe otra etiqueta,

	<span> </span>

Para salto de línea, que no de párrafo ya que no guarda márgenes,

	<br> </br>

## LOS TITULARES Ó ENCABEZADOS

Los clasificamos por orden de importancia semántica con las siguientes etiquetas,

	<h1> </h1> Visualmente y nivel de importancia es mayor
	<h2> </h2>
	<h3> </h3>
	<h4> </h4>
	<h5> </h5>
	<h6> </h6> Visualmente y nivel de importacia es el menor de todos.

Como mínimo en la web hay dos h1 que son el logo y el titular principal. No se le puede poner a todo h1 ya que aplana la semántica y Seo y Google no te tendrán en cuenta.

Existe una etiqueta que sirve como símil a caja y no aporta nada semánticamente. Se utiliza para envoltura de contenido sin connotación alguna,

	<div> </div>

## MODELO DE CAJA: content-box (clásico)

Los bordes (border) en éste modelo de caja son exterior, crecen hacia fuera y es ahí cuando empieza el margen (margin). La unión del borde, si lo ponemos en distintos colores, se verá en inglete a 45º. Saber hacer ésto te permite hacer polígonos en CSS y así conseguimos que éstas imagenes no pesen nada ya que no hay imágenes adicionales. Más tarde en CSS definiremos el grosor, estilo de línea y color.

Dentro de los bordes hay un área de relleno que deja respirar al texto que se llama padding, al igual que los bordes, hay que definir que hay padding top (la parte de arriba), padding bottom (la parte de abajo), padding right (parte derecha), padding left (parte izquierda). Algunas etiquetas ya vienen con un padding mayor a 0 automático.

El ancho de la etiqueta empieza (width) se inicia con los contenidos y el alto (heigh) de inicio a fin de contenido.


## MODELO DE CAJA: border-box

La diferencia en cuanto a la anterior es el alto y el ancho de la caja que, en éste caso, empieza en el borde exterior.

El borde y el padding crecen de fuera hacia dentro, no como en el anterior.

Por defecto, se adaptan los elementos de bloque, en ancho, a todo y en alto al contenido. el head, body y html son elementos de bloque. El body tiene un padding de fábrica y el html se adapta a la ventana.


## SITIOS DONDE ESCRIBIR CSS

Existen tres sitios, in line (en la línea del código), una etiqueta style en el head ó la más utilizada en el 99´5% de los casos, en un archivo CSS.

    - In line: Sólo se utiliza cuando no es una página web, por ejemplo un newletter (un html incrustado en un email), en la línea de texto del HTML,

	<p style= "color:red"> texto...</p>

    - Poner una etiqueta del CSS dentro del head,

	<style>
		p{   (cada propiedad en una línea)
		    color:red; 
			background-color: cyan;
		}
	</style>


# CSS

		/-----------------CSS----------------/
	index.html		galeria.html	contactos.html

Se abre un archivo nuevo CSS y se guarda. Éste afectará a todos los archivos HTML vinculándolo con una etiqueta link en el head de HTML que no se cierra,

	<link href= "css/css.css" rel= "stylesheet">

El atributo href marca la ruta del archivo CSS.
 