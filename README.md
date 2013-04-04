![Simpletastic](http://i.imgur.com/gHeZUdr.png)

Simplestastic is a super lightweight framework (actually just **a few lines** of code) written in Sass that greatly simplifies the creation of fluid grids on responsive enviroments. It is designed for people tired of complex frameworks with tons of, sometimes, useless options, who want to write something quick and simple.

Forget about calculating weird percentages or using magic numbers, inspired by [this article](http://csswizardry.com/2013/02/responsive-grid-systems-a-solution/) by Harry Roberts, instead of defining a class name like `.span-3` or `.large-6`, which has little meaning and is not very easy to memorize, let Simpletastic abstract these widths into comprehensible human-friendly fractions. For example: you can have 3 columns of which every one is **one third** of the available space `@include column (1, 3)`, or **one half** `@include column (1, 2)`, or even **four twelfths** `@include column (4, 12)`. Any combination that suits your needs is possible.

It uses `display: inline-block` to place elements, so everything can be aligned vertically and horizontally.

### Requirements

- Sass 3.2+ (Silent classes are used, which means that the classes never get compiled to CSS until they are explicitly expanded into another class.)

## Getting started

In your main stylesheet:

```sass
@import "grid";
```

Then just 2 steps, without any previous configuration :)

1. Extend the `%row` invisible class to any `.class-name` or `<tag>` that is going to be the container for the columns. This is basically a clear-fix.

    ```scss
    @extend %row;
    ```
2. And include the `column` mixin in the child element(s). In this case one third of the available space.

    ```scss
    @include column(1 of 3);
    ```

    ![Simple](http://i.imgur.com/ClDn51U.png)

## Options

1. **Nesting**. For nested columns instead of using the mixin `columns`, it would be `nested-columns` adding a new `paramenter` with the parent fractions, like this:

    ```scss
    @include nested-column(1 of 2, 3 of 4);
    ```

    ![Nested](http://i.imgur.com/QZRKQso.png)

2. **Automatic Rows**. Only for this case an extra `@include` which removes the `margin-right` every `N` times is needed:

    ```scss
    @include row-each(1);
    ```

    ![Automatic Rows](http://i.imgur.com/SnJFuq2.png)

## Settings

The only default setting is the `gutter` size which, by default, is set to `2%`, can be overridden. Any percentage value, including `0` to remove it, can be used.

```scss
$default-gutter-width: 2% !default;
```

You can also override the `gutter` for any column by simply passing the new size to the column mixin using a third parameter.

```scss
li { @include column(1 of 3, 0%); }

// Or…

li { @include column(1 of 3, 10%); }
```

## Support

Honestly I didn't do too many compatibility testing. But I would say major modern browsers can handle it pretty much perfect.

### Author

Fran Pérez [@mrrocks](http://twitter.com/mrrocks)