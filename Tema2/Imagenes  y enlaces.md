# Imagenes y enlaces
A1. Verdadero o falso
N.º |	V / F |	Respuesta y corrección
----|-------|-----------------------
1	| "La etiqueta "img" se cierra con "/img"." |	No	"img" es una etiqueta vacía y no se cierra.
2	| "El atributo alt muestra un texto si la imagen no se puede cargar." |	Sí	Además, lo leen los lectores de pantalla y los buscadores.
3	| "Para dar ancho y alto a una imagen se recomienda usar style en lugar de width y height." |	Sí	Así el tamaño es CSS y no lo cambia sin querer una hoja de estilos.
4	| "La propiedad float permite que una imagen flote a la izquierda o a la derecha del texto, o que no flote." | Sí	Valores left, right y none.
5	| "El rótulo de un enlace solo puede ser un texto." |	No	El rótulo puede ser un texto, una imagen o las dos cosas.
6	| "target="_blank" hace que el enlace se abra en una ventana (pestaña) nueva."	| Sí	Sin target, se abre en la misma ventana.
7	| "Por defecto, un enlace ya visitado se ve azul y uno por visitar, morado."	| No	Es al revés: por visitar, azul y subrayado; visitado, morado.
8	| "Un enlace relativo escribe la URL completa, incluido el dominio."	| No	Eso es un enlace absoluto. El relativo indica la ruta desde la página actual (paginas/contacto.html).


A2. Relaciona atributo y función
Elemento |	Descripción |	Respuesta
---------|--------------|-----------
1. src | D. Ruta del archivo de imagen | 1-D
2. alt | G. Texto que se muestra si la imagen no carga | 2-G
3. href | B. Indica el destino del enlace |	3-B
4. target |	F. Indica dónde se abrirá el destino del enlace | 4-F
5. id | A. Crea un marcador (bookmark) dentro de la página | 5-A
6. float |	E. Propiedad CSS para que la imagen flote junto al texto |	6-E
7. _blank |	C. Valor de target que abre una pestaña nueva |	7-C


A3. ¿Absoluto o relativo?
N.º |	Dirección |	Tipo |	Por qué
----|-----------|------|---------
1 |	https://www.w3.org/ |	Absoluto |	Lleva protocolo y dominio.
2 |	paginas/contacto.html	| Relativo |	Ruta desde la carpeta de la página actual.
3	| /css/default.asp |	Relativo (a la raíz) |	Empieza por /: se busca desde la carpeta raíz del sitio web, pero sin dominio.
4 |	https://www.google.com/ |	Absoluto |	Lleva protocolo y dominio.
5	| ./apuntes.pdf | Relativo	| ./ significa "la carpeta actual".
6 |	imagenes/logo.png	| Relativo |	Entra en la subcarpeta imagenes.


A4. Formatos de imagen
Abreviatura |	Nombre completo |	Extensión
------------|-----------------|----------
GIF |	Graphics Interchange Format |	.gif
JPEG |	Joint Photographic Experts Group |	.jpg, .jpeg
PNG |	Portable Network Graphics |	.png
SVG |	Scalable Vector Graphics |	.svg
ICO	| Microsoft Icon |	.ico
APNG |	Animated Portable Network Graphics |	.apng


A5. Caza los errores de la galería
````
"!DOCTYPE html"
"html"
"head"
"meta charset="utf-8""
"title"Mi galería"/title"
"/head"
"body"
"h1"Mi viaje de fin de curso"/h1"
"img"src="playa.jpg" alt="Playa al atardecer""/img"
"img src="monte.jpg" style="width=300px; height=200px;""
"a href=https://www.wikipedia.org target="_blank""Más información sobre el destino
"/body"
"/html"
````
Errores
1	"img"src="playa.jpg" ...	Los atributos están fuera de la etiqueta: se cierra "img" y luego se escriben como texto.	"img src="playa.jpg" alt="Playa al atardecer""
2	"/img"	"img" no se cierra.	Quitar "/img".
3	width=300px; height=200px;	En CSS, propiedad y valor se separan con :, no con =.	width:300px; height:200px;
4	Segunda imagen sin alt	Todas las imágenes deben llevar alt.	alt="Vista del monte"
5	Enlace sin cerrar	Falta "/a": el enlace no termina nunca.	Añadir "/a".
6	href=https://... sin comillas	Las normas del curso piden poner siempre los valores entre comillas.	href="https://www.wikipedia.org"
7	Falta lang y meta author	Mejora y norma del boletín.	"html lang="es"" y "meta name="author""


El validador del W3C confirma los errores 1 a 5.
Aqui está la versión corregida
````
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Mi galería"/title"
"/head"
"body"
  "h1"Mi viaje de fin de curso"/h1"
  "img src="playa.jpg" alt="Playa al atardecer""
  "img src="monte.jpg" alt="Vista del monte" style="width:300px; height:200px;""
  "a href="https://www.wikipedia.org" target="_blank""Más información sobre el destino"/a"
"/body"
"/html"
````
A6. Rutas que no funcionan
El código está en index.html, en la carpeta proyecto/.
Código	¿Funciona?	Motivo	Corrección
"img src="logo.png" alt="Logo""	No	logo.png está dentro de imagenes/.	src="imagenes/logo.png"
"img src="imagenes/equipo.jpg" alt="Equipo""	Sí		
"a href="Contacto.html""Contacto"/a"	No	El archivo es contacto.html en minúsculas, y en muchos servidores no es lo mismo.	href="contacto.html"
"a href="apuntes.pdf""Apuntes"/a"	Sí		
"a href="imagenes/apuntes.pdf""Apuntes"/a"	No	apuntes.pdf no está en imagenes/, sino junto a index.html.	href="apuntes.pdf"
"img src="imagenes/equipo.png" alt="Equipo""	No	La foto es .jpg, no .png.	src="imagenes/equipo.jpg"


En Windows, Contacto.html puede funcionar al abrir la página desde tu ordenador, porque no distingue mayúsculas, pero falla al subirla a un servidor Linux.
A7. ¿Qué verá el usuario?
"h2"Mi mascota"/h2"
"img src="gato.jpg" alt="Gato durmiendo" style="float: right;""
"p"Se llama Miau y duerme catorce horas al día. Cuando está despierto, intenta apagar el router."/p"
"a href="https://www.w3.org/" target="_blank"""img src="logo.png" alt="W3C"""/a"
(a) La imagen del gato aparece a la derecha, a la altura del párrafo, y el texto queda a su izquierda rodeándola.

(b) Si gato.jpg no existe, en su lugar sale el icono de imagen rota con el texto "Gato durmiendo" (el alt), también a la derecha.

(c) Al hacer clic en el logo se abre https://www.w3.org/ en una pestaña nueva, porque el rótulo del enlace es la imagen y lleva target="_blank".

(Comprobación: copia el código en un .html, ábrelo y pega aquí tu captura.)
Nivel 2 · B1. Galería de tu setup
" Todos los ejercicios van en la carpeta boletin_html2/, con las imágenes en boletin_html2/imagenes/.
"
" Muestra tres veces la misma imagen: a tamaño original; a 200 × 150 px con el atributo style; y a 200 × 150 con los atributos width y height. Todas con alt. Después rompe a propósito el nombre de una en el src y observa qué se muestra. Pregunta (en un comentario): ¿por qué se recomienda style frente a width y height?
Código: b1.html
````
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"B1. Galería de tu setup"/title"
"/head"
"body"
  "h1"Galería de mi setup"/h1"
  "h2"Tamaño original"/h2"
  "img src="imagenes/setup.jpg" alt="Mi escritorio con el ordenador y los periféricos""
  "h2"200 × 150 con el atributo style"/h2"
  "img src="imagenes/setup.jpg" alt="Mi escritorio con el ordenador y los periféricos" style="width:200px; height:150px;""
  "h2"200 × 150 con los atributos width y height"/h2"
  "img src="imagenes/setup.jpg" alt="Mi escritorio con el ordenador y los periféricos" width="200" height="150""
  "h2"Imagen rota a propósito"/h2"
  "img src="imagenes/setp.jpg" alt="Mi escritorio con el ordenador y los periféricos""
  "!--
    Pregunta: ¿por qué se recomienda style frente a width y height?
    Respuesta: con style el tamaño pasa a ser CSS, como el resto del aspecto de la página.
    Así no lo puede cambiar sin querer una hoja de estilos y todo el diseño está en el mismo sitio.
  --"
"/body"
"/html"
````
Qué se ve con la imagen rota
El src apunta a setp.jpg, que no existe. En lugar de la foto, el navegador muestra el icono de imagen rota junto al texto del alt. Por eso el alt debe describir la imagen.
Respuesta a la pregunta
Con style el tamaño pasa a ser CSS, como el resto del aspecto de la página. Así no lo puede cambiar sin querer una hoja de estilos y todo el diseño queda en el mismo sitio. Los atributos width y height siguen siendo válidos.
Qué recordar
- "img" no se cierra. Lleva src (ruta de la imagen) y alt (texto alternativo).
- Con style se pone la unidad: width:200px;. Con los atributos, solo el número: width="200".
Nivel 2 · B2. Perfil de una red social
" Todos los ejercicios van en la carpeta boletin_html2/, con las imágenes en boletin_html2/imagenes/.
"
" Un "h1" con el nombre del creador; una foto de perfil con borde de 5 px verde continuo y float: right; tres párrafos de biografía que rodeen la imagen; una segunda imagen con float: left y borde punteado azul; y una tercera con float: none y sin borde. Pregunta: ¿qué diferencia visual hay entre left, right y none?
Código: b2.html
````
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"B2. Perfil de una red social"/title"
"/head"
"body"
  "h1"Lucía Pixel"/h1"
  "img src="imagenes/perfil.jpg" alt="Foto de perfil de Lucía Pixel" style="width:180px; border:5px solid green; float:right;""
  "p"Lucía Pixel es creadora de contenido sobre tecnología desde 2019. Empezó grabando vídeos cortos sobre cómo montar un ordenador por piezas y hoy tiene una comunidad de miles de seguidores que la acompañan cada semana en sus directos."/p"
  "p"En su canal explica de forma sencilla cómo elegir componentes, cómo cuidar la seguridad de las cuentas y cómo sacar partido a programas gratuitos. Sus vídeos favoritos son los de comparativas, en los que pone a prueba dos productos durante una semana."/p"
  "p"Cuando no está grabando, estudia un ciclo de informática y participa en torneos de videojuegos con su equipo. Su lema es que cualquiera puede aprender tecnología si se lo explican con paciencia."/p"
  "img src="imagenes/setup.jpg" alt="El escritorio de Lucía" style="width:160px; border:3px dotted blue; float:left;""
  "p"Este es el escritorio desde el que graba todos sus vídeos: dos pantallas, un micrófono de condensador y un teclado mecánico con interruptores silenciosos para que no se oiga en los directos. Además, ha colocado una lámpara de luz cálida detrás de las pantallas para cansar menos la vista cuando graba por la noche. Todo el cableado va recogido por detrás de la mesa para que en cámara se vea ordenado."/p"
  "p""img src="imagenes/logo.png" alt="Logo del canal de Lucía" style="width:120px; float:none;"" Este es el logo del canal. No flota: se queda en la línea del texto, como si fuera una letra más."/p"
"/body"
"/html"
````
Respuesta a la pregunta
- float: left: la imagen se pega a la izquierda y el texto la rodea por la derecha.
- float: right: la imagen se pega a la derecha y el texto la rodea por la izquierda.
- float: none (el valor por defecto): la imagen no flota. Se queda en su sitio dentro del texto y este no la rodea.
Qué recordar
- Para que se note que el texto rodea la imagen, el párrafo tiene que ser más largo que la imagen. Si no, pon la imagen más pequeña con width.
- Borde: border: grosor estilo color; → border:5px solid green;.
Nivel 2 · B3. ¿Qué formato elijo?
" Todos los ejercicios van en la carpeta boletin_html2/, con las imágenes en boletin_html2/imagenes/.
"
" Escribe cinco párrafos, cada uno con una necesidad, e indica con "strong" el formato recomendado y su extensión: foto de vacaciones con muchos colores; logo con fondo transparente; icono nítido a cualquier tamaño; animación corta tipo meme; icono de la pestaña del navegador. Incluye al menos dos imágenes de formatos distintos.
Código: b3.html
````
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"B3. ¿Qué formato elijo?"/title"
"/head"
"body"
  "h1"¿Qué formato de imagen elijo?"/h1"
  "p"Para una foto de vacaciones con muchos colores: "strong"JPEG (.jpg)"/strong", porque comprime bien las fotografías y ocupa poco."/p"
  "p"Para un logo con fondo transparente: "strong"PNG (.png)"/strong", porque admite transparencia y no pierde calidad."/p"
  "p"Para un icono que se vea nítido a cualquier tamaño: "strong"SVG (.svg)"/strong", porque es vectorial y no se pixela al ampliarlo."/p"
  "p"Para una animación corta tipo meme: "strong"GIF (.gif)"/strong", porque admite animación y lo abre cualquier navegador."/p"
  "p"Para el icono de la pestaña del navegador: "strong"ICO (.ico)"/strong", el formato clásico del favicon."/p"
  "h2"Ejemplos"/h2"
  "img src="imagenes/setup.jpg" alt="Ejemplo de fotografía en JPEG" style="width:240px;""
  "img src="imagenes/logo.png" alt="Ejemplo de logo en PNG" style="width:160px;""
  "img src="imagenes/meme.gif" alt="Ejemplo de animación en GIF" style="width:160px;""
"/body"
"/html"
````
Qué recordar
Necesidad	Formato
Fotografía con muchos colores	JPEG (.jpg)
Fondo transparente	PNG (.png)
Nítido a cualquier tamaño	SVG (.svg)
Animación	GIF (.gif) o APNG (.apng)
Icono de la pestaña (favicon)	ICO (.ico)


Nivel 2 · B4. Mis enlaces favoritos
" Tres enlaces a webs reales, cada uno en su "p": uno a https://www.w3.org/ en la misma ventana, uno a https://www.google.com/ en ventana nueva y uno a tu elección en ventana nueva. Cambia el color de uno con style. Pregunta: ¿de qué color se ve por defecto un enlace por visitar y uno ya visitado?
Código: b4.html
````
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"B4. Mis enlaces favoritos"/title"
"/head"
"body"
  "h1"Mis enlaces favoritos"/h1"
  "p""a href="https://www.w3.org/""W3C, el organismo que crea los estándares web"/a""/p"
  "p""a href="https://www.google.com/" target="_blank""Google, en una pestaña nueva"/a""/p"
  "p""a href="https://developer.mozilla.org/es/" target="_blank" style="color:darkorange;""MDN, documentación de HTML y CSS"/a""/p"
"/body"
"/html"
````
Respuesta a la pregunta
Por defecto, un enlace por visitar se ve azul y subrayado, y uno ya visitado, morado. Mientras se pulsa (enlace activo), se ve rojo.
Qué recordar
Atributo	Para qué sirve
href	Destino del enlace
sin target (o target="_self")	Se abre en la misma ventana
target="_blank"	Se abre en una pestaña nueva


Nivel 2 · B5. Enlaces con imagen
" Todos los ejercicios van en la carpeta boletin_html2/, con las imágenes en boletin_html2/imagenes/.
"
" Un enlace cuyo rótulo es solo una imagen (a una web externa, en pestaña nueva) y otro cuyo rótulo es una imagen y un texto a la vez. En un comentario, identifica el destino, el rótulo y el objetivo de cada enlace.
Código: b5.html
````
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"B5. Enlaces con imagen"/title"
"/head"
"body"
  "h1"Enlaces con imagen"/h1"
  "p""a href="https://www.w3.org/" target="_blank"""img src="imagenes/logo.png" alt="Ir a la web del W3C" style="width:150px;"""/a""/p"
  "p""a href="https://developer.mozilla.org/es/"""img src="imagenes/icono.svg" alt="Icono de MDN" style="width:32px;"" Documentación de MDN"/a""/p"
  "!--
    Enlace 1: destino https://www.w3.org/, rótulo la imagen logo.png, objetivo _blank (pestaña nueva).
    Enlace 2: destino https://developer.mozilla.org/es/, rótulo la imagen icono.svg y el texto
    "Documentación de MDN", objetivo la misma ventana (no lleva target).
  --"
"/body"
"/html"
````
Partes de un enlace
	Enlace 1	Enlace 2
Destino (href)	https://www.w3.org/	https://developer.mozilla.org/es/
Rótulo (lo que se pulsa)	La imagen logo.png	La imagen icono.svg y el texto "Documentación de MDN"
Objetivo (target)	_blank: pestaña nueva	Sin target: misma ventana


Qué recordar
- El rótulo es todo lo que va entre "a" y "/a": un texto, una imagen o las dos cosas.
- Si el rótulo es solo una imagen, su alt debe decir adónde lleva el enlace ("Ir a la web del W3C").
Nivel 2 · B6. Mini web de tres páginas
" Todos los ejercicios van en la carpeta boletin_html2/, con las imágenes en boletin_html2/imagenes/.
"
" Crea index.html, sobre-mi.html y contacto.html, cada una con un "h1" distinto y un menú con enlaces relativos a las otras dos. En index.html, una imagen de la subcarpeta imagenes; en contacto.html, un enlace absoluto a una web externa. Pregunta: ¿qué enlaces dejarían de funcionar si movieras contacto.html a otra carpeta?
Código: index.html
````
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Inicio"/title"
"/head"
"body"
  "h1"Bienvenido a mi web"/h1"
  "p""a href="sobre-mi.html""Sobre mí"/a" | "a href="contacto.html""Contacto"/a""/p"
  "img src="imagenes/logo.png" alt="Logo de mi web" style="width:200px;""
  "p"Esta es la página principal de mi mini web."/p"
"/body"
"/html"
Código: sobre-mi.html
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Sobre mí"/title"
"/head"
"body"
  "h1"Sobre mí"/h1"
  "p""a href="index.html""Inicio"/a" | "a href="contacto.html""Contacto"/a""/p"
  "p"Estudio 2.º de SMR y me gusta la informática y los videojuegos."/p"
"/body"
"/html"
Código: contacto.html
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Contacto"/title"
"/head"
"body"
  "h1"Contacto"/h1"
  "p""a href="index.html""Inicio"/a" | "a href="sobre-mi.html""Sobre mí"/a""/p"
  "p"Puedes ver mis proyectos en "a href="https://github.com/" target="_blank""GitHub"/a"."/p"
"/body"
"/html"
````
Respuesta a la pregunta
Si contacto.html se mueve a otra carpeta (por ejemplo, paginas/), dejan de funcionar:
- Los enlaces de index.html y sobre-mi.html que apuntan a contacto.html, porque ya no está en la misma carpeta (habría que poner paginas/contacto.html).
- Los enlaces del menú de contacto.html a index.html y sobre-mi.html, porque ahora tendrían que subir una carpeta (../index.html).
El enlace absoluto a GitHub sigue funcionando, porque lleva la dirección completa.
Qué recordar
- Relativo: ruta desde la página actual (sobre-mi.html, imagenes/logo.png). ../ sube una carpeta.
- Absoluto: dirección completa con el dominio (https://github.com/).
Nivel 2 · B7. Tu propia chuleta
" Haz una chuleta de una página con lo aprendido hasta ahora y guárdala en PDF. Crea chuleta.html con un "h1" y tres enlaces: al PDF local en la misma ventana, al PDF local en pestaña nueva y a un recurso con URL externa. Pregunta: ¿qué pasa si borras el PDF de la carpeta?

chuleta.pdf va en la misma carpeta que chuleta.html.
Código: chuleta.html
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"B7. Mi chuleta"/title"
"/head"
"body"
  "h1"Mi chuleta de HTML"/h1"
  "p""a href="chuleta.pdf""Abrir la chuleta en esta ventana"/a""/p"
  "p""a href="chuleta.pdf" target="_blank""Abrir la chuleta en una pestaña nueva"/a""/p"
  "p""a href="https://developer.mozilla.org/es/docs/Web/HTML" target="_blank""Documentación de HTML en MDN"/a""/p"
"/body"
"/html"
Respuesta a la pregunta
Si se borra chuleta.pdf, los dos enlaces locales dejan de funcionar: el navegador muestra un error de archivo no encontrado (en un servidor web, el error 404). El enlace externo a MDN sigue funcionando, porque no depende de tu carpeta.
Qué recordar
- Un enlace puede llevar a cualquier archivo, no solo a páginas: PDF, imágenes, documentos...
- El navegador abre el PDF en su propio visor.
Nivel 2 · Parte C. Práctica 2. Las estaciones (enlaces e imágenes)
" Crea una página estaciones.html con 4 imágenes de 300 × 300 píxeles que sean enlaces a otono.html, invierno.html, primavera.html y verano.html. Estas páginas también las creas tú, con la estructura base, un "h1" con el nombre de la estación, la foto en grande (600 × 600) y un enlace de vuelta a estaciones.html.
"
" - estaciones.html: "h1" con el texto ESTACIONES; después, un "h2" con el título de cada estación y su foto a 300 × 300 (no recortes la imagen). Cada foto lleva un borde de 5 píxeles de un color distinto. Al hacer clic en la foto se abre la página de la estación en la misma ventana.
" - Cada página de estación: título, foto a 600 × 600 con borde del mismo color que en la página principal y, debajo, un enlace con el texto "Volver a la página principal".
" - Todas las imágenes llevan atributo alt.
Reflexión previa
1. ¿Qué ruta relativa usará estaciones.html para cargar primavera.jpg?

imagenes/primavera.jpg: desde la carpeta de estaciones.html se entra en imagenes y se coge el archivo.

2. ¿Qué pasaría si movieras las páginas de cada estación a una carpeta paginas/?

Se romperían las rutas. Esas páginas tendrían que subir una carpeta para encontrar las fotos (../imagenes/primavera.jpg) y para volver (../estaciones.html), y estaciones.html tendría que enlazar a paginas/primavera.html.

3. Si las fotos miden 600 × 600 y deben verse a 300 × 300, ¿las recortas o cambias el tamaño con HTML/CSS?

Cambio el tamaño con CSS (width:300px; height:300px;). Así se usa la misma foto en las dos páginas, no se pierde ninguna parte y, como es cuadrada, no se deforma.
Estructura de ficheros
estaciones/
├── imagenes/
│   ├── primavera.jpg
│   ├── verano.jpg
│   ├── otono.jpg
│   └── invierno.jpg
├── estaciones.html
├── primavera.html
├── verano.html
├── otono.html
└── invierno.html
Fotos de licencia libre de al menos 600 px de ancho: Unsplash, Pixabay o Wikimedia Commons. Si no son cuadradas, recórtalas a 600 × 600 antes de guardarlas para que no se deformen.
Colores de los bordes
Estación	Color
Primavera	mediumseagreen
Verano	gold
Otoño	chocolate
Invierno	steelblue


Código: estaciones.html

````
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Estaciones"/title"
"/head"
"body"
  "h1"ESTACIONES"/h1"
  "h2"Primavera"/h2"
  "a href="primavera.html"""img src="imagenes/primavera.jpg" alt="Foto de primavera" style="width:300px; height:300px; border:5px solid mediumseagreen;"""/a"
  "h2"Verano"/h2"
  "a href="verano.html"""img src="imagenes/verano.jpg" alt="Foto de verano" style="width:300px; height:300px; border:5px solid gold;"""/a"
  "h2"Otoño"/h2"
  "a href="otono.html"""img src="imagenes/otono.jpg" alt="Foto de otoño" style="width:300px; height:300px; border:5px solid chocolate;"""/a"
  "h2"Invierno"/h2"
  "a href="invierno.html"""img src="imagenes/invierno.jpg" alt="Foto de invierno" style="width:300px; height:300px; border:5px solid steelblue;"""/a"
"/body"
"/html"
Código: primavera.html
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Primavera"/title"
"/head"
"body"
  "h1"Primavera"/h1"
  "img src="imagenes/primavera.jpg" alt="Foto de primavera" style="width:600px; height:600px; border:5px solid mediumseagreen;""
  "p""a href="estaciones.html""Volver a la página principal"/a""/p"
"/body"
"/html"
Código: verano.html
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Verano"/title"
"/head"
"body"
  "h1"Verano"/h1"
  "img src="imagenes/verano.jpg" alt="Foto de verano" style="width:600px; height:600px; border:5px solid gold;""
  "p""a href="estaciones.html""Volver a la página principal"/a""/p"
"/body"
"/html"
Código: otono.html
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Otoño"/title"
"/head"
"body"
  "h1"Otoño"/h1"
  "img src="imagenes/otono.jpg" alt="Foto de otoño" style="width:600px; height:600px; border:5px solid chocolate;""
  "p""a href="estaciones.html""Volver a la página principal"/a""/p"
"/body"
"/html"
Código: invierno.html
"!DOCTYPE html"
"html lang="es""
"head"
  "meta charset="utf-8""
  "meta name="author" content="Claudio""
  "title"Invierno"/title"
"/head"
"body"
  "h1"Invierno"/h1"
  "img src="imagenes/invierno.jpg" alt="Foto de invierno" style="width:600px; height:600px; border:5px solid steelblue;""
  "p""a href="estaciones.html""Volver a la página principal"/a""/p"
"/body"
"/html"
````

# Nivel 3 · Parte A

## A1. Verdadero o falso

| N.º | Afirmación | V / F | Respuesta y corrección |
|---|---|---|---|
| 1 | "Para crear un bookmark se añade el atributo `id` a una etiqueta de la página." | **V** | Por ejemplo, `<h2 id="precios">`. |
| 2 | "`<a href="#S4">` salta al elemento con `id="S4"` de la misma página." | **V** | El `#` indica un marcador de la página. |
| 3 | "Dos elementos de la misma página pueden tener el mismo `id`." | **F** | El `id` debe ser **único** en cada página. |
| 4 | "`<a href="guia.html#wifi>` abre `guia.html` directamente en la sección con ese "id"." | V | Abre la página y salta al elemento con "id="wifi"". |
| 5 | "Los identificadores "Precios" y "precios" son el mismo." | F | Los "id" distinguen mayúsculas y minúsculas: son dos identificadores distintos. |

## A2. ¿Qué pasa al hacer clic?

````
<!-- Caso A -->
<a href="#precios">Ver precios</a>
<h2 id="precios">Precios</h2>

<!-- Caso B -->
<a href="#Precios">Ver precios</a>
<h2 id="precios">Precios</h2>

<!-- Caso C -->
<a href="guia.html#instalacion">Ir a la instalación</a>
````

| Caso | Qué pasa |
|------|----------|
| A | La página salta al título "Precios", porque "#precios" coincide con "id="precios"". |
| B | No salta. "#Precios" lleva la P mayúscula y el "id" es "precios": no coinciden. La página se queda donde está. |
| C | Se abre "guia.html" en la misma ventana y salta directamente a la sección con "id="instalacion". Si esa sección no existe, se abre al principio de la página. |

Los casos A y B los he comprobado en el navegador.

A3. Reflexiona

1. ¿En qué tipo de páginas resulta más útil un índice con bookmarks?**

En las páginas **largas** con varias secciones: guías, manuales, apuntes, preguntas frecuentes (FAQ), artículos o documentación técnica. Así el lector va directo a lo que busca sin desplazarse por toda la página.

2. Al final de cada sección habrá un enlace de vuelta al índice. ¿A qué `id` debe apuntar y dónde tienes que ponerlo?**

Debe apuntar al `id` que está en la **parte de arriba, donde está el índice** (por ejemplo, `<h1 id="inicio">`), con `<a href="#inicio">Volver arriba</a>`. El `id` se pone una sola vez arriba, y el enlace se repite **al final de cada sección**.

3. ¿Qué pasaría si dos secciones tuvieran el mismo `id`?**

El HTML sería **incorrecto** (el validador lo marca como error) y el enlace saltaría solo a la **primera** sección con ese `id`. A la segunda no se podría llegar con el índice.

Nivel 3 · B1. Guía exprés de ciberseguridad en casa

> Crea `guia.html`: un `<h1 id="inicio">`; un **índice** con cuatro enlaces (separados con `<br>`) a las secciones contraseñas, Wi-Fi, actualizaciones y copias de seguridad; cuatro secciones `<h2>` con su `id` y al menos dos párrafos cada una (la página debe ser lo bastante larga para tener que desplazarse); y al final de cada sección un enlace "Volver arriba" a `#inicio`. Crea además `indice.html` con un enlace que lleve **directamente a la sección Wi-Fi** de `guia.html`.

Código: guia.html

````
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>Guía exprés de ciberseguridad</title>
</head>
<body>
  <h1 id="inicio">Guía exprés de ciberseguridad en casa</h1>
  <h2>Índice</h2>
  <p>
    <a href="#contrasenas">Contraseñas</a><br>
    <a href="#wifi">Wi-Fi</a><br>
    <a href="#actualizaciones">Actualizaciones</a><br>
    <a href="#copias">Copias de seguridad</a>
  </p>
  <h2 id="contrasenas">Contraseñas</h2>
  <p>Una buena contraseña es larga: cuantos más caracteres tenga, más difícil es adivinarla. Una frase de varias palabras que solo tú entiendas, de al menos 12 caracteres, es más segura que una palabra corta llena de símbolos.</p>
  <p>No repitas la misma contraseña en varias webs. Si una de ellas sufre una filtración, los atacantes probarán esa contraseña en todas tus cuentas. Un gestor de contraseñas las recuerda por ti y crea contraseñas distintas para cada sitio.</p>
  <p>Activa la verificación en dos pasos siempre que puedas. Así, aunque alguien consiga tu contraseña, necesitará además un código de tu móvil para entrar.</p>
  <p>Desconfía de cualquier correo o mensaje que te pida tu contraseña, aunque parezca de tu banco o de tu instituto. Ninguna empresa seria te la pedirá nunca por correo: es la técnica del phishing.</p>
  <p><a href="#inicio">Volver arriba</a></p>
  <h2 id="wifi">Wi-Fi</h2>
  <p>Lo primero al instalar un router es cambiar la contraseña de administración que trae de fábrica, porque suele estar publicada en internet y cualquiera podría entrar en su configuración.</p>
  <p>Usa el cifrado WPA2 o, mejor, WPA3, con una clave larga, y desactiva el WPS, que facilita que alguien se conecte sin conocer la clave.</p>
  <p>Si vienen visitas, ofréceles una red de invitados. Así navegan sin tener acceso a tus ordenadores, impresoras o cámaras.</p>
  <p>Revisa de vez en cuando la lista de dispositivos conectados en la configuración del router. Si aparece alguno que no reconoces, cambia la clave de la Wi-Fi.</p>
  <p><a href="#inicio">Volver arriba</a></p>
  <h2 id="actualizaciones">Actualizaciones</h2>
  <p>Las actualizaciones no solo traen funciones nuevas: sobre todo corrigen fallos de seguridad que los atacantes ya conocen. Retrasarlas deja la puerta abierta.</p>
  <p>Activa las actualizaciones automáticas del sistema operativo, del navegador y de las aplicaciones del móvil. Y no te olvides del router: también tiene su propio software, llamado firmware.</p>
  <p>Descarga los programas solo de la web oficial o de la tienda de aplicaciones. Las versiones "gratis" de programas de pago suelen esconder malware.</p>
  <p>Cuando un dispositivo deja de recibir actualizaciones, como un móvil muy antiguo, es mejor no usarlo para la banca o el correo, porque sus fallos ya no se van a corregir.</p>
  <p><a href="#inicio">Volver arriba</a></p>
  <h2 id="copias">Copias de seguridad</h2>
  <p>Una copia de seguridad es la única forma de recuperar tus fotos y trabajos si el disco se estropea, si pierdes el móvil o si un ransomware cifra tus archivos.</p>
  <p>Sigue la regla 3-2-1: tres copias de tus datos, en dos soportes distintos (por ejemplo, el ordenador y un disco externo) y una de ellas fuera de casa o en la nube.</p>
  <p>De vez en cuando, prueba a restaurar algún archivo. Una copia que nunca se ha comprobado puede fallar justo cuando más la necesitas.</p>
  <p>Programa las copias para que se hagan solas, por ejemplo una vez por semana. Las copias que dependen de acordarse acaban por no hacerse.</p>
  <p><a href="#inicio">Volver arriba</a></p>
</body>
</html>
````

Código: "indice.html"

````
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Claudio">
  <title>Índice de guías</title>
</head>
<body>
  <h1>Guías de la clase</h1>
  <p><a href="guia.html#wifi">Ir directamente a la sección Wi-Fi de la guía de ciberseguridad</a></p>
</body>
</html>
````

Cómo funciona

| Pieza | Código | Qué hace |
|-------|--------|----------|
Marcador | `<h2 id="wifi">` | Pone un "nombre" a ese punto de la página |
Enlace en la misma página | `<a href="#wifi">` | Salta a ese marcador |
Volver arriba | `<a href="#inicio">` | Salta al `<h1 id="inicio">` |
Enlace a otra página | `<a href="guia.html#wifi">` | Abre `guia.html` directamente en la sección Wi-Fi |


Parte C

````
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Stranger Things 4</title>
</head>

<body>

    <h1 id="inicio">Stranger Things 4</h1>

    <h2>Índice</h2>

    <ul>
        <li><a href="#introduccion">Introducción</a></li>
        <li><a href="#trailer">Tráiler</a></li>
        <li><a href="#fecha">Fecha de estreno</a></li>
        <li><a href="#reparto">Reparto</a></li>
        <li><a href="#argumento">Argumento</a></li>
    </ul>

    <hr>

    <h2 id="introduccion">Introducción</h2>

    <p>
        La temporada 4 de Stranger Things tiene algunas preguntas importantes que responder después del explosivo final de 77 minutos de la temporada 3, 'La batalla de Starcourt'. Pero no desesperen, amigos. La serie de ciencia ficción de Netflix regresará para la cuarta temporada, lo que significa que todos esos cabos sueltos por los que has estado perdiendo el sueño se resolverán. Sigue leyendo mientras nos ponemos nuestra ropa más brillante con un tema de los 80, enciende el electropop y sumérgete en todo lo relacionado con Hawkins, Indiana. Aquí está todo lo que necesitas saber sobre la cuarta temporada de Stranger Things.
    </p>

    <p><a href="#inicio">Volver al índice</a></p>

    <hr>

    <h2 id="trailer">Tráiler</h2>

    <p>
        Netflix lanzó su último avance teaser en mayo de este año. En el clip, nos llevan al laboratorio donde el Dr. Brenner realizó sus experimentos con niños, vistos por última vez en flashbacks en las temporadas uno y dos. Un reloj siniestro hace tic tac de fondo; los niños persiguen carros de juguete alrededor de una pista de arcoíris (¿recuerdan la habitación del arco iris de la segunda temporada?); alguien está jugando al ajedrez; una bola cae a través de alfileres en un tablero de clavijas; se dice "las señales apuntan a sí"; hay una risa infantil espeluznante; ladrillos de juguete; todo tiene mucho eco y está iluminado en el gris verdoso institucional que hemos llegado a esperar de las malas agencias gubernamentales experimentales.
    </p>

    <p>
        Todos los niños tienen la cabeza rapada y batas de hospital como solía hacer Once en la primera temporada. Es evidente que hemos retrocedido en el tiempo porque vemos al Dr. Martin Brenner (desde atrás, pero se le reconoce en cualquier lugar) acechando los pasillos, y mientras la voz de Matthew Modine les dice a los niños: "Tenemos algo muy especial planeado para vosotros hoy", la cámara hace un zoom inquietante en una puerta marcada como '11'. El tráiler termina con la voz en off que dice: "¿Once? ¿Estás escuchando?". y los ojos de la joven Once se abren de repente por la sorpresa.
    </p>

    <p><a href="#inicio">Volver al índice</a></p>

    <hr>

    <h2 id="fecha">Fecha de estreno</h2>

    <p>
        Actualmente no hay una fecha de estreno oficial sobre la mesa, aunque ahora sabemos que la cuarta temporada no llegará hasta 2022. Un teaser reciente solo confirmó que regresará el próximo año, lo que es significativamente más tarde de lo que esperábamos. El productor Shawn Levy aprecia que la cuarta temporada esté tardando más de lo esperado, incluido él, pero promete que "vale la pena esperar". "Sólo diré que estamos muy retrasados, y los Duffers y yo queremos compartir la cuarta temporada con el mundo tanto como el mundo lo desee", dijo a The Hollywood Reporter. "Parte de lo que está tomando tiempo es mucho antes de que existieran COVID y la pandemia, la cuarta temporada se construyó para ser, con mucho, la temporada más ambiciosa, cinematográfica, extensa y épica que hayamos hecho".
    </p>

    <p><a href="#inicio">Volver al índice</a></p>

    <hr>

    <h2 id="reparto">Reparto</h2>

    <p>
        La serie no sería la serie que es sin su reparto, así que volverán a sus pantallas una vez más: Once (Millie Bobby Brown), Mike (Finn Wolfhard), Lucas (Caleb McLaughlin), Dustin (Gaten Matarazzo), Will (Noah Schnapp), Max (Sadie Sink), Steve (Joe Keery), Nancy (Natalia Dyer), Jonathan (Charlie Heaton), Robin (Maya Hawke) y Joyce (Winona Ryder), entre otros.
    </p>

    <p>
        Todos sabemos ahora que David Harbour regresará como Hopper, a pesar de ese final aparentemente trágico de la tercera temporada. En una charla con Total Film, Harbour explicó que su personaje "tenía que cambiar" y "resucitar de alguna manera", y agregó: "Así que veremos a un tipo muy diferente avanzando. El mismo tipo pero en una vena diferente. Es muy algo genial para poder jugar". Si bien aún no está claro cómo sobrevivió su personaje, Harbour ha revelado que la cuarta temporada revelará más de su historia en una llamada a la segunda temporada, donde Once encontró cajas en el ático de Hopper etiquetadas como "papá", "Vietnam" y "Nueva York".
    </p>

    <p>
        Myles Truitt interpretará el papel del jugador de baloncesto de Hawkins, Patrick, cuya vida terminará "saliéndose de control" después de algunos "eventos impactantes", mientras que Amybeth McNulty interpretará a Vickie, descrita como "una banda nerd genial y de habla rápida que llama la atención de uno de nuestros queridos héroes". "Fui una de las primeras personas de mi grupo de amigos en ver la primera temporada de Stranger Things", le dijo a The Times. "Cuando me seleccionaron, grité, lloré y me emocioné mucho".
    </p>

    <p><a href="#inicio">Volver al índice</a></p>

    <hr>

    <h2 id="argumento">Argumento</h2>

    <p>
        "Honestamente, los guiones son geniales", dijo Natalia Dyer a The Independent cuando se le preguntó sobre los próximos episodios. "Cada vez que terminamos una temporada, todos pensamos, '¿A dónde va a ir esto? ¿A dónde puede ir esto?' Luego obtenemos los guiones para la próxima temporada y pensamos, '¡Dios mío, wow, como, wow!'. Ella agregó: "Va a ser realmente grande. ¡Va a ser grande!".
    </p>

    <p>
        Hablando con MTV, Sink sonó igualmente emocionado: "Es una temporada increíble. Y la escala es tan enorme este año. Creo que la gente realmente la va a disfrutar". Matarazzo también habló sobre cómo ha cambiado la serie en la cuarta temporada con Entertainment Tonight. "Cuando se trata del tono de la temporada, definitivamente, creo que el tono definitivamente ha madurado, y creo que ellos [los creadores Matt y Ross Duffer] lo hacen a propósito porque creo que quieren que su serie madure con su niños", explicó. "A medida que envejecemos como personas, tenemos que envejecer como personajes. Se enfrentan a este problema, pero lo abrazan y lo usan para su ventaja. Y no se asustan cuando nos hacemos más altos o cuando nuestras voces bajan o algo por el estilo. Lo usan y lo usan como munición para su escritura. Es increíble lo que pueden hacer. Trabajar con ellos, es simplemente excepcional. Siempre lo ha sido".
    </p>

    <p>
        La tercera temporada concluyó con una nota extremadamente emocional. Joyce, Will y Jonathan empacaron su casa en Hawkins y se subieron a una camioneta de mudanzas con Once a cuestas después de la muerte de Hopper (que en realidad no fue una muerte). "No todo son buenas noticias para nuestro 'estadounidense'; está encarcelado lejos de casa en el páramo nevado de Kamchatka, donde enfrentará peligros tanto humanos ... como de otro tipo", se lee en la sinopsis oficial de Netflix. "Mientras tanto, de vuelta en los Estados Unidos, un nuevo horror está comenzando a aflorar, algo enterrado hace mucho tiempo, algo que conecta todo ...".
    </p>

    <p><a href="#inicio">Volver al índice</a></p>

    <hr>

</body>
</html>
````
