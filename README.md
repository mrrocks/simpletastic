Simpletastic - Fluid Grid
============

Simplestastic es un pequeño framework escrito en SASS (.scss) que facilita enormemente la creación de grids fluidas.

Uso

```css
.container { %extend %grid__row; }

.column { @include grid-column(1, 3); }
```