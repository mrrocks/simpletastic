Simpletastic - Fluid Grid System
============

Simplestastic es un pequeño framework escrito en SASS (.scss) que facilita enormemente la creación de grids fluidas.

###Basic Use - Just 2 steps :)

```scss

// First. Extend the row invisible class to any class or object is going to contain the columns

    .container { @extend %grid__row; }

// Include to define the column with, in this case one third of the available space

    .column { @include grid-column(1, 3); }
```