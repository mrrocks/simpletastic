Simpletastic
============

Simplestastic is a very lightweight framework (actually just a few lines of code) written in Sass that greatly simplifies the creation of responsive and fluid grids. It is designed for people tired of complex frameworks with tons of, sometimes, useless options, who want to write something quick and simple.

Forget about calculating weird percentages or using some magic numbers, inspired by [this article](http://csswizardry.com/2013/02/responsive-grid-systems-a-solution/) by Harry Roberts, instead of defining a class name like `.span-3` or `.large-6`, which has little meaning and is not very easy to memorize, let Simpletastic abstract these widths into comprehensible fractions. For example: If you wanted to have 3 columns of which every one was **one third** of the available space `@include column (1, 3)`, or **one half** `@include column (1, 2)`, or even **four twelfths** `@include column (4, 12)`. Any combination that suits your needs is possible.


### Requirements

- Sass 3.2+ (Silent classes are used, which means that the classes never get compiled to CSS until they are explicitly expanded into another class.)

### Getting started

In your main stylesheet:

```sass
@import "grid";
```

Then just 2 steps :)

1. Extend the `%row` invisible class to any `.class-name` or `<tag>` that is going to be the container for the columns.

    ```scss
    ul {
        @extend %row;
    }
    ```
2. Then include the `column` mixin in the child element(s). In this case one third of the available space.

    ```scss
    li {
        @include column(1, 3);
    }
    ```

    ![Example 1](http://i.imgur.com/XZZNtXj.png)

### Settings

The only default setting is the `gap` size which, by default, is set to `2%`, can be overridden. Any percentage value, including `0` to remove it, can be used.

```scss
$default-gap-width: 2% !default;
```

You can also override the gap size for any column by simply passing the new size to the column mixin using the third parameter.

```scss
li { @include column(1, 3, 0%); }

// Or…

li { @include column(1, 3, 10%); }
```
