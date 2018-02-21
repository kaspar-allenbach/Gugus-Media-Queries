# Gugus Media-Queries
A simple Media Query Library for Sass to go. (Gugus: Swiss German for «peeck a boo»)

These queries are an adaption of [David Walshes Media Query Mixins](https://davidwalsh.name/write-media-queries-sass)

Import ins SCSS with: `@import "../../node_modules/gugus-media-queries/gugus-media-queries";`

There are Size Variables to easily change the mixins. These Sizes are based on [Bootstrap 4](https://getbootstrap.com/docs/4.0/layout/grid/#grid-options)

| Size           | px      | Example Selector      | Example Selector (downwards) |
| -------------- |:-------:| ---------------------:| ----------------------------:|
| Extra small    | <576px  | `none required`       | `none required`      |
| Small          | ≥576px  | `@include smUp { … }` | `@include smDown { … }`      |
| Medium         | ≥768px  | `@include mdUp { … }` | `@include mdDown { … }`      |
| Large          | ≥992px  | `@include lgUp { … }` | `@include lgDown { … }`      |
| Extra large    | ≥1200px | `@include xlUp { … }` | `@include XLDown { … }`      |


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
.hiddenLgDown {
  @include smDown {
    display: none;
  }
}
```
This would hide an element on Lg size and below.
You can now add Visibility Classes as a extend, asa Mixin or as a class directly in th HTML:
