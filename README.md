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

1. Extend the `%row` invisible class to any `.class-name` or `<tag>` that is going to be the container for the columns.

    ```scss
    ul { @extend %row; }
    ```
2. Include in the child element/s the `column` mixin to define the column width, in this case one third of the available space.

    ```scss
    li { @include column(1, 3); }
    ```