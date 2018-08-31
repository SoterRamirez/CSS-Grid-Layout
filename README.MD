# Curso de CSS Grid Layout

![Meme](https://i.imgflip.com/1c7cy8.jpg)
:bowtie:

Clase 2

## ¿Qué es CSS grids?

El diseño de cuadrícula CSS o cuadrícula CSS es una técnica en CSS que permite a los desarrolladores web crear diseños de diseño web complejos y receptivos de forma más fácil y consistente en todos los navegadores.

Clase 3

## Conceptos fundamentales sobre CSS Grid Layout

[Documentación oficial de MDN](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Grid_Layout)

[Otra link](https://css-tricks.com/snippets/css/complete-guide-grid/)

**Grid Container**: va a ser el elemento padre que va a tener puesto un nuevo tipo de display: grid. Nos permite colocar otras propiedades para manipular nuestro layaout.

Ejemplo:

```
<div class="container">
    <div class="item item-1"></div>
    <div class="item item-2"></div>
    <div class="item item-3"></div>
</div>
```

**Grid Item**: Son nuestro componentes, contenido, lo que vamos a manejar. Nuestras filas o columnas que vamos a mover a nuestro gusto. Son hijos directos de grid.

Ejemplo:

```
<div class="container">
    <div class="item"></div>
    <div class="item">
        <p class="sub-item"></p>
    </div>
    <div class="item"></div>
</div>
```

**Grid Line**: Lineas divisorias horizontales y verticales.

**Grid Track**: Espacio entre dos líneas adyacentes. Filas y columnas.

**Grid Cell**: Celdas, espacio en dos filas adyacentes y 2 columnas adyacentes.

**Grid Area**: Espacio rodeado por 4 grid lines

Clase 4

# Definiendo columnas :sunglasses:

![Definiendo columnas](https://cdn.scotch.io/1/lD6AXrDYSA26ZoveE7Nz_uTQ64cA.png)

Creamos una carpeta "Columna" y dentro "index.html"

Designar columnas :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Columnas</title>
  <style>
    body {
      font-family: Arial;
    }
    .container {
      display: grid;
      grid-template-columns: 25% 200px 25%;
    }
    .item {
      background: lightblue;
      padding: 10px;
      border: 1px solid red;
    }
  </style>
</head>
<body>
  <section class="container">
    <div class="item">contenido #1</div>
    <div class="item">contenido #2</div>
    <div class="item">contenido #3</div>
    <div class="item">contenido #4</div>
    <div class="item">contenido #5</div>
    <div class="item">contenido #6</div>
    <div class="item">contenido #7</div>
    <div class="item">contenido #8</div>
    <div class="item">contenido #9</div>
    <div class="item">contenido #10</div>
    <div class="item">contenido #11</div>
    <div class="item">contenido #12</div>
  </section>
</body>
</html>
```

Clase 5 :alien:
# Definiendo filas

Carpeta: "Filas", Archivo: "index.html"

Para definir las filas:

```grid-template-rows: valores;```

Definir filas y columnas:

```grid-template: filas / columnas;```

**grind implicito**: Es cuando tenemos filas y/o columnas que no definimos pero forman parte de nuestro grid

**grid explicito**:  Es cuando definimos el numero de columnas y/o filas.

Clase 6
# Grids identados y tipos de displays :neckbeard:

Carpeta: "Displays", Archivo: "index.html"

Display subgrid para heredar la configuración del grid padre (cuando se esten anidando grids).

```display: subgrid; // No disponible aun```


Display inline-grid muestra el grid en una sola linea:

```display: inline-grid; // No disponible aun```


Clase 7
# Espaciado entre filas y columnas :frowning:

/play secret

:warning: Importante: Chrome 66 hizo cambios en css-grid, específicamente en gap y ahora es simplemente gap:

Espaciado entre columnas
```
column-gap: value;
```
Espaciado entre filas
```
row-gap: value;
```
Espaciado entre filas y columnas
```
gap: rows columns;
```