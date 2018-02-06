# Gugus-Media-Queries
A simple Media Query Library for Sass

These queries are an adaption of David Walshes Media Query Mixins
https://davidwalsh.name/write-media-queries-sass

There are Size Variables to easily change the mixins. (These Sizes are based on Bootstrap)

```
$xl-width: '1200px';
$lg-width: '992px';
$md-width: '786px';
$sm-width: '576px';
```

### Example of usage:

```
@include smUp {
  body {
    background: red;
  }
};
```
### Compiles to
```
@media (min-width: 576px) {
  body {
    background: red;
    }
};
```
