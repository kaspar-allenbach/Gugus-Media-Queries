# Gugus Media-Queries
A simple Media Query Library for Sass to go.

These queries are an adaption of [David Walshes Media Query Mixins](https://davidwalsh.name/write-media-queries-sass)

Import ins SCSS with: `@import "../../node_modules/gugus-media-queries/gugus-media-queries";`

There are Size Variables to easily change the mixins. These Sizes are based on [Bootstrap 4](https://getbootstrap.com/docs/4.0/layout/grid/#grid-options)

| Size           | px      | SCSS Variable             | Example Selector      | Example Selector (downwards) |
| -------------- |:-------:| -------------------------:| ---------------------:| ----------------------------:|
| Extra small    | <576px  | `No Media Query required` | `none required`       | `none required`      |
| Small          | ≥576px  | `$sm-width: '576px';`     | `@include smUp { … }` | `@include smDown { … }`      |
| Medium         | ≥768px  | `$md-width: '768px';`     | `@include mdUp { … }` | `@include mdDown { … }`      |
| Large          | ≥992px  | `$lg-width: '992px';`     | `@include lgUp { … }` | `@include lgDown { … }`      |
| Extra large    | ≥1200px | `$xl-width: '1200px';`    | `@include xlUp { … }` | `@include XLDown { … }`      |


# Example of usage 

#### foo.scss
```
@include smUp {
  body {
    background: red;
  }
};
```
#### Compiles to
```
@media (min-width: 576px) {
  body {
    background: red;
    }
};
```
There are visibility Extends as well:
```
%hiddenLgDown {
  @include smDown {
    display: none;
  }
}
```
This would hide an element on Lg size and below.

#### Known Issues:

The way SCSS works `%extends` are not possible within the media query scope like this. So yeah. That's not great. Looking for a solution.
