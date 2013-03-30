Simpletastic - Fluid Grid System
============

Simplestastic is a super lightweight framework written in SASS that make it super easy create to fluid grids.

Requirements
===
- Sass 3.2+

Install Instructions
===

In your main stylesheet:

```sass
@import "grid";
```

###Basic Use - Just 2 steps :)

```sass
/* First: Extend "%grid__row" invisible class to any .class or <object> that is going to contain the columns */

    ul { @extend %grid__row; }

/* Second: Include the mixin that defines the column with, in this case one third of the available space */

    li { @include grid-column(1, 3); }
```