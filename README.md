# XY (float)

> XY (float) is a small and very flexible collection of mixins for building grids based on floating elements.

## What is?

This is a collection of mixins for all preprocessors (Less, Stylus, Sass), which you can use to create a grid that is convenient for you and your project.

If you need to set only the width of columns - you just do it. Later you can add offset, push or pull for the columns using the appropriate mixin.

## WTF? Where flexbox?

Coming soon in **XY (flexbox)**.

## How to use

Just import the file, which includes mixins in your project.

```less
// Less
@import "lib/xy";
// Sass
@import "lib/xy";
// Stylus
@import "lib/xy";
```

## Mixins

  * [xy-make-container](#xy-make-container)
  * [xy-make-container-width](#xy-make-container-width)
  * [xy-make-row](#xy-make-row)
  * [xy-make-column](#xy-make-column)
  * [xy-make-columns-width (offset, push, pull)](#xy-make-columns-width-offset-push-pull)
  * [xy-make-grid-columns](#xy-make-grid-columns)

### xy-make-container

> Creates a container

Parameters:

  * **gutter** - distance between columns

### xy-make-container-width

> Defines of the maximum width for the container

Parameters:

  * **breakpoint** - device breakpoint
  * **width** - container width

### xy-make-row

> Creates a row

Parameters:

  * **gutter** - distance between columns

### xy-make-column

> Creates a column

Parameters:

  * **gutter** - distance between columns

### xy-make-columns-(width, offset, push, pull)

> Defines of width (offset, push or pull) for the column

Parameters:

  * **alias** - column alias
  * **count** - the number of columns

### xy-make-grid-columns

> Generator complete collection of styles for a single alias

Parameters:

  * **alias** - column alias
  * **breakpoint** (optional) - device breakpoint
  * **count** - the number of columns

## Examples

**Example for Less**

```less
// Container
.container {
  .xy-make-container(30px);
  .xy-make-container-width(768px, 720px);
  .xy-make-container-width(992px, 960px);

  .row {
    .xy-make-row(30px);
  }
}

// Column
.col {
  .xy-make-column(30px);
  .xy-make-grid-columns(xs, 12);
  .xy-make-grid-columns(sm, 768px, 12);
  .xy-make-grid-columns(md, 992px, 12);
}
```

More examples for all preprocessors can be seen in the [tests](https://github.com/mrmlnc/xy/tree/master/tests) directory.

## License

MIT.
