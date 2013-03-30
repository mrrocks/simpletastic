Simpletastic - Fluid Grid System
============

Simplestastic es un pequeño framework escrito en SASS (.scss) que facilita enormemente la creación de grids fluidas.

###Basic Use - Just 2 steps :)

```scss
// First: Extend "%grid__row" invisible class to any .class or <object> that is going to contain the columns

    ul { @extend %grid__row; }

// Second: Include the mixin that defines the column with, in this case one third of the available space

    li { @include grid-column(1, 3); }
```

```html
<ul>
    <li>Column of one third</li>
    <li>Column of one third</li>
    <li>Column of one third</li>
</ul>
```