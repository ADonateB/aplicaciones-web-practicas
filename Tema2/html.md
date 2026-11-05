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
