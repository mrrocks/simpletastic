Simpletastic
============

Simplestastic is a very lightweight framework (actually just a few of lines of code) written in Sass that greatly simplifies the creation of responsive and fluid grids. It is designed for people tired of complex frameworks with tons and sometimes useless options, who want to write something quick and simple.

Forget about calculating weird percentages or use some magic numbers, inspired by [this article](http://csswizardry.com/2013/02/responsive-grid-systems-a-solution/) by Harry Roberts, instead of defining a class name like `.span-3` or `.large-6`, which has little meaning and it is not very easy to memorize, Simpletastic abstracts these widths into comprehensible fractions. For example: you would like to do 3 columns of which every one is **one third** of the available space `@include column (1, 3)`, or **one half** `@include column (1, 2)`, or even **four twelfths** `@include column (4, 12)`. Any combination that suits your needs is possible.


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
2. Then choose any possible combinationInclude in the child element/s the `column` mixin to define the column width, in this case one third of the available space.

    ```scss
    li {
        @include column(1, 3);
    }
    ```

    ![Example 1](http://i.imgur.com/5nVsVU9.png)

### Settings

The only default setting is the `gap` size, by default is set to `2%`, but you can override this and use any percentage value, including `0` to remove it.

```scss
$default-gap-width: 2% !default;
```

Also you can override the gap size for any column, just optionally pass to the column mixin the size as the third parameter.

```scss
li { @include column(1, 3, 0%); }

// Or…

li { @include column(1, 3, 10%); }
```
