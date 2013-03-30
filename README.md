Simpletastic
============

Simplestastic is a super lightweight framework written in SASS that make it super easy create to fluid grids.

### Requirements

- Sass 3.2+

### Install Instructions

In your main stylesheet:

```sass
@import "grid";
```

###Getting started

Just 2 steps :)

1. Extend "%grid__row" invisible class to any .class or <object> that is going to contain the columns

```scss
ul { @extend %grid__row; }
```
2. Include the mixin that defines the column width, in this case one third of the available space

```scss
li { @include grid-column(1, 3); }
```