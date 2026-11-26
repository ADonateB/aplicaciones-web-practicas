Horario en html

````
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        table, th, td {
            border: 1px solid black;
            border-collapse: collapse;
        }

        th {
            background-color: grey;
        }
        td {
            padding: 10px;
        }
    </style>
</head>

<body>
    <caption>Horario de SMX</caption>
    <table>
        <tr>
            <th>Desde-Hasta</th>
            <th>Lunes</th>
            <th>Martes</th>
            <th>Miercoles</th>
            <th>Jueves</th>
            <th>Viernes</th>
        </tr>
        <tr>
            <th>14:00-15:00</th>
            <td>Programacion</td>
            <td></td>
            <td>Programación</td>
            <td></td>
            <td>Programación</td>
        </tr>

        <tr>
            <th>15:00-15:55</th>
            <td>IPE</td>
            <td>App Web</td>
            <td>Servicios en Red</td>
            <td>Servicios en Red</td>
            <td>Servicios en Red</td>
        </tr>

        <tr>
            <th>15:55-16:50</th>
            <td>Seguridad Informatica</td>
            <td>Servicios en Red</td>
            <td>Servicios en Red</td>
            <td>Servicios en Red</td>
            <td>Projecto Intermodular</td>
        </tr>

        <tr>
            <th>16:50-17:45</th>
            <td>Seguridad Informatica</td>
            <td>Servicios en Red</td>
            <td>Seguridad Informatica</td>
            <td>App Web</td>
            <td>SOR</td>
        </tr>

        <tr>
            <th>18:05-19:00</th>
            <td>Sostenibilidad</td>
            <td>IPE</td>
            <td>Seguridad Informatica</td>
            <td>App Web</td>
            <td>SOR</td>
        </tr>

        <tr>
            <th>19:00-19:55</th>
            <td>SOR</td>
            <td>IPE</td>
            <td>Digitalizacion</td>
            <td>SOR</td>
            <td>SOR</td>
        </tr>

        <tr>
            <th>19:55-20:50</th>
            <td></td>
            <td>Projecto Intermodular</td>
            <td></td>
            <td>SOR</td>
            <td></td>
        </tr>
    </table>
</body>

</html>
````
