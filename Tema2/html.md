#Actividad 1, Hacer tabla y decir si son verdaderas, falsas y corregir las falsas
N.º  |  Afirmación  |  V/F  |
|----|--------------|-------|
1 |"HTML es un lenguaje de programación como Python: sirve para hacer cálculos y tomar decisiones."|F, es un lenguaje de marcado
2 |"La etiqueta ´br´´<br>´ no necesita etiqueta de cierre."|V
3 |"El valor de un atributo siempre se escribe entre comillas."|V
4 |"Los atributos de una etiqueta se escriben en la etiqueta de cierre."|F,los atributos se escriben en la etiqueta de apertura
5 |"El texto de ´title´´<title>´ aparece en la pestaña del navegador."|V
6 |`strong y b´<strong>´ y ´<b>´ se visualizan igual.|V
7 |"Todo lo que escribimos dentro de ´head´´<head>´ se ve en la página."|V
8 |"La etiqueta ´hr´´<hr>´ se cierra con </hr>."|V
9 |"Un comentario HTML ´<!-- ... -->´´(<!-- ... -->)´ se muestra en pantalla como una nota gris."|F, solo se ve si entras en inspeccionar, no sale en la pantalla del navegador.
10 |"´span´<span>´ crea un bloque de texto que siempre empieza en una línea nueva."|F, span no empieza en una linea nueva ni genera saltos de linea, se queda en la misma fila

#Actividad 2, hacer esta pequeña tabla y unir cada comando con lo que hace
Etiqueta  |  |  Efecto  |
|---------|--|----------|
1.mark |2 |Texto tachado (precio antiguo de una oferta)  |
2.del |1 |Texto remarcado, como con un fosforito  |
3.sub |6 |Texto enfatizado (se ve como cursiva)  |
4.sup |5 |Texto más pequeño que el normal  |
5.small |3 |Texto en subíndice (como en H₂O)  |
6.em |4 |Texto en superíndice (como en m²)  |
7.ins |7 |Texto insertado (se ve subrayado)  |

#Actividad 3, encontrar los fallos en este código
<html>
<head>
<title>Mi tienda de gadgets
</head>
<body>
<h1>Ofertas de otoño</h2>
<p>Auriculares con <b>cancelación de ruido</p></b>
</body>
</html>

": es para que salgan los comandos para ver cuales estan mal

Falta cerrar el title: "/title"
Abres el "h1" pero cierras con "/h2", cuando no cierras el h1 y no abres el h2
El head se cierra antes del título, porque como el título no está cerrado todo lo que hay se sigue considerando parte del título
Cierras el "/b" cuando ni si quiera ha sido abierto

#Actividad 4 Explicar que falla y corregir

<h1 style="color:red font-size:40px;">Directo esta noche</h1>
<p style="text-align=center;">Estreno de temporada</p>
<p style="background-color:yellow;">Sorteo de una tarjeta gráfica<p>

En "color:red le falta un ; para acabar con el tema del color y empezar el tamaño
en text-align no se pone un igual, se pone un : para que ponga align:center
No cierras la última "/p"

Actividad 5 encontrar y corregir errores

<!- Revisar el texto antes de publicar ->
<p>Tu contraseña debe tener <strong><em>al menos 12 caracteres</strong></em>.</p>

Al principio para empezar hay que poner dos -- despues del ! y para cerrar tambien hay que poner dos --
Para que salga la ñ debes poner un comando antes UTF-8
Los comandos strong y em estan cerrados al reves: "/em""/strong"

Actividad 6 Pon que le mostrara al usuario el navegador

<h1>Resumen de la jornada</h1>
<p>Ha ganado el equipo local.<br>El rival se despide del torneo.</p>
<hr>
<h4>Próximo partido</h4>
<p>Sábado a las 18:00</p>

# Fin de la parte A

### Código parte B

````<!DOCTYPE html>
<html lang="en">
<head>
    <title>Plantilla de 2.ºSMR</title>
    <meta charset="UTF-8">
    <meta name="Alvaro" content="Ejercicios parte B">
    <title>Document</title>
</head>
<body>
<!-- Aqui va el contenido -->
    <h1>¿La IA te quitará el trabajo?</h1>
    <h2>Hoy hablaremos sobre la IA y su evolución</h2>
    <p>La IA es una herramienta muy usada últimamente</p>
    <p>Es muy útil en muchos aspectos</p>
    <hr>
    <p>Hay que tener mucho cuidado con el uso de la IA</p>

    Autor: Alvaro <br>
    Fecha: 15/11/2026 <br>
    Fuente: Elaboración propia <br>
<hr>
    <h2>Pruebas de tamaños</h2>
    <h1>Este es h1</h1>
    <h2>Este es h2</h2>
    <h3>Este es h3</h3>
    <h4>Este es h4</h4>
    <h5>Este es h5</h5>
    <h6>Este es h6</h6>

    <hr>
<!-- ¿Que diferencia hay entre <b> y <strong>? y entre <i> y <em>? 
    <b> pone el texto en negrita
    <strong> tambien lo pone en negrita pero le da importancia tambien
    <i> pone el texto en cursiva
    <em> pone el texto en cursiva pero tambien le da importancia
    -->


    <h2>BLACK FRIDAY</h2>
    <h3>Iphone 17</h3>
    <p><b>Tienda de hermanos informáticos</b></p>
    <i>Compra ahora el mejor precio</i>
    <p>Con garantia de <em>1 año</em></p>
    <p>Rápido porque solo hay <mark>250 unidades</mark> y 100 unidades <small>Pequeñas y ligeras</small> para no llevar una gran carga</p>
    <p>Antes: <del>1500€</del> ahora: <strong>999€</strong></p>
    <p>Apunta:<ins>Cº Toledo</ins> y el nombre de la tienda</p>
    <p>Si te gastas más de <u>1200€</u> se te regala accesorios para los productos que lleves</p>
    <p>Y recuerda: Tienda<sub>de</sub>hermanos<sup>informáticos</sup></p>

    <hr>

    <h1 style="background-color: lightblue;">Banner del streamer</h1>
    <h2 style="text-align: center;">Este es el texto centrado</h2>
    <h3 style="text-align: right; background-color: limegreen; font-size: 150%;">Texto a la derecha</h3>

    <hr>

    <!-- El #3cb371 es color verde
         El (238, 130, 238) es color rosa  -->
    <!-- El rgb(0, 0, 255) solo color azul (0 rojo, 0 verde y 255 azul)-->
    <h2 style="color: red;">Rojo Estandar</h2>
    <h2 style="color: rgb(255, 0, 0);">Rojo con Rgb</h2>
    <h2 style="color: #f00;">Rojo con Hex</h2>
    <h2 style="color: hsl(0, 100%, 50%);">Rojo con HSL</h2>
    <h2 style="color: orange;">Naranja Estandar</h2>
    <h2 style="color: rgb(255, 165, 0);">Naranja con Rgb</h2>
    <h2 style="color: #ffa500;">Naranja con Hex</h2>
    <h2 style="color: hsl(39, 100%, 50%);">Naranja con Hsl</h2>
    <h2 style="color: #3cb371;">Que color es #3cb371</h2>
    <h2 style="color: rgb(238, 130, 238);">Que color es rgb(238, 130, 238)</h2>

    <hr>

    <!-- Se usan fuentes para que sea más atractivo y que la gente mire las opciones que hay para comprar-->
    <h2> Menu del restaurante de ramen</h2>
    <h3 style="font-family: sans-serif;">Restaurante de ramen</h3>
    <h3 style="font-family: monospace;">9€ el tazón</h3>
    <h3 style="font-family: FuenteInventada, Arial, sans-serif;">Picante</h3>

    <hr>

    <h1 style="border: 5px solid green;">Cartel de festival</h1>
    <p style="border: 3px dotted blue;">Preparate para el festival</p>
    <p style="background-color: lightpink; border: 5px double red;">Entradas a 6€</p>

    <hr>

    <!--Diferencia entre span y p
    P: es paea crear un párrafo completo
    Span: es para crear un párrafo pero que todo este en la misma línea
    -->
    <h1 style="border: 5px solid green;">Festival de música</h1>
    <p style="border: 3px dotted blue;">Ven al festival a disfrutar</p>
    <p style="background-color: lightpink; border: 5px double red;">Entradas a 5€</p>
    <p>Artistas destacados:
        <span style="color: blue; font-size: 200%;">Quevedo</span>
        <span style="color: green; font-size: 200%;">Porta</span>
    </p>

    <hr>

    <!--Primero se abre b, i, u
    Se cierra al reves, ya que primero hay que cerrar lo que se ha abierto más recientemente: u, i, b-->
    <p>
        <b>
            <i>
                <u>
                    ALERTA DE SERVICIO DE SEGURIDAD
                </u>
            </i>
        </b>
    </p>

    <hr>
   
</body>
</html>
````

# Parte C
### El texto tiene 8 párrafos y debe verse justificado. ¿Qué etiqueta usarás para cada uno y qué propiedad CSS consigue la justificación?

Usaré un "p" para cada párrafo
Usaré el text-align: justify

### Los comentarios de los personajes irán en cursiva y los sentimientos, en color y negrita. ¿Qué etiquetas sirven para marcar solo una parte de un párrafo?

Usaré "i" para que sea en cursiva
Usaré "span" para cambiar el color
Usaré "b" para poner el texto en negrita

### Un mismo sentimiento debe tener siempre el mismo color. ¿Cómo evitas equivocarte? (Pista: haz antes una lista de sentimientos y colores.)

Evito equivocarme mirando la lista y no repitiendo colores

Sentimiento  |  Color
-------------|-------
Alegria | verde
Tristeza | azul
Enfado | rojo
Miedo | morado


### Codigo parte C

````
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
<h2 style="text-align: center; border: 1px solid purple;">
    EL AMOR Y LA LOCURA
</h2>

<p style="text-align: justify;">
Cuentan que una vez se reunieron en un lugar de la Tierra todos los sentimientos y
cualidades de los hombres. Cuando el aburrimiento había bostezado por tercera vez,
la locura, como siempre tan loca, les propuso: <i>"¿Jugamos al escondite?"</i>.
La intriga levantó la ceja intrigada y la curiosidad, sin poder contenerse,
preguntó: <i>"¿Al escondite? ¿Y cómo es eso?"</i>.
<i>"Es un juego -explicó la locura- en el que yo me tapo la cara y comienzo a contar
desde uno hasta un millón mientras ustedes se esconden. Y, cuando yo haya terminado
de contar, el primero de ustedes al que encuentre ocupará mi lugar para continuar
el juego".</i>
</p>

<p style="text-align: justify;">
El entusiasmo bailó secundado por la euforia. La
<b><span style="color: green;">alegría</span></b> dio tantos saltos que terminó
por convencer a la duda e, incluso a la apatía, a la que nunca le interesaba nada.
Pero no todos quisieron participar; la verdad prefirió no esconderse, ¿para qué?,
si, al final, siempre la hallaban; y la soberbia opinó que era un juego muy tonto,
pero en el fondo, lo que le molestaba es que la idea no hubiese sido suya.
Y la cobardía... la cobardía prefirió no arriesgarse.
<i>"Uno, dos, tres..."</i>, comenzó a contar la locura.
</p>

<p style="text-align: justify;">
La primera en esconderse fue la pereza que, como siempre, se dejó caer en la primera
piedra del camino. La fe subió al cielo y la envidia se escondió tras la sombra
del triunfo que con su propio esfuerzo había logrado subir a la copa del árbol
más alto. La generosidad casi no alcanzaba a esconderse, cada sitio que hallaba
le parecía maravilloso para alguno de sus amigos: que si un lago cristalino,
ideal para la belleza; que si una rendija de un árbol, perfecto para la timidez;
que si el vuelo de una mariposa, lo mejor para la voluptuosidad; que si una ráfaga
de viento, magnífico para la libertad. Así que terminó por ocultarse en un rayito
de sol. El egoísmo, en cambio, encontró un sitio muy bueno desde el principio;
lo encontró ventilado, cómodo... pero eso sí, sólo para él. La mentira se escondió
en el fondo de los océanos, ¡mentira! en realidad se escondió detrás del arco iris.
Y la pasión y el deseo en el centro de los volcanes. El olvido... ¡se me olvidó
dónde se escondió! pero, bueno, eso no es lo importante.
</p>

<p style="text-align: justify;">
Cuando la locura contaba 999.999, el amor aún no había encontrado sitio para
esconderse, pues todo se encontraba ocupado, hasta que divisó un rosal y,
enternecido, decidió esconderse entre sus flores.
</p>

<p style="text-align: justify;">
<i>"Un millón"</i> contó la locura, y comenzó a buscar. La primera en aparecer fue
la pereza, sólo a tres pasos de la piedra. Después escuchó a la fe discutiendo
con Dios en el cielo sobre teología. Y la pasión y el deseo los sintió en el vibrar
de los volcanes. En un descuido encontró al triunfo y, claro, pudo deducir dónde
estaba la envidia. Al egoísmo no tuvo ni que buscarlo, él solito salió disparado
desde su escondite, que había resultado ser un nido de avispas.
</p>

<p style="text-align: justify;">
De tanto caminar sintió sed y, al acercarse al lago, descubrió a la belleza.
Y con la duda resultó más fácil todavía, pues la encontró sentada sobre una cerca
sin decidir aún en qué lado esconderse.
</p>

<p style="text-align: justify;">
Así fue encontrando a todos: la mentira detrás del arco iris, ¡mentira! estaba
en el fondo del océano; y hasta el olvido, al que ya se le había olvidado que
estaba jugando al escondite. Pero, sólo el amor no aparecía por ninguna parte.
La locura buscó detrás de cada árbol, bajo cada rolluelo del planeta, en la cima
de las montañas; y, cuando estaba por darse por vencida, divisó un rosal y sus rosas,
y tomó una horquilla y comenzó a mover sus ramas bruscamente. Cuando, de pronto...
un doloroso grito se escuchó. Las espinas habían herido en los ojos al amor.
La locura no sabía qué hacer para disculparse: lloró, rogó, imploró, pidió perdón
y hasta prometió ser su Lazarillo.
</p>

<p style="text-align: justify;">
<span style="display: block; font-size: 2em; color: white; background-color: darkred; font-weight: bold;">
EL AMOR ES CIEGO Y LA LOCURA SIEMPRE LE ACOMPAÑA.
</span>
</p>


<p style="text-align: justify;">
<span style="display: block; font-size: 2em; color: white; background-color: darkred; font-weight: bold;">
EL AMOR ES CIEGO Y LA LOCURA SIEMPRE LE ACOMPAÑA.
</span>
</p>

</body>
</html>
````
