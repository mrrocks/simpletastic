Simpletastic - Fluid Grid
============

Simplestastic es un pequeño framework escrito en SASS (.scss) que facilita enormemente la creación de grids fluidas.

#Basic Use

```scss

// Extend

    .container { %extend %grid__row; }

// Include to define the column with, in this case one third of the available space

    .column { @include grid-column(1, 3); }
```