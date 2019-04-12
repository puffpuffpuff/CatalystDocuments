# Catalyst Website Documentation
Documentation for common code used in website development.
Click :arrow_double_up: to navigate back into table of content.

## Table of content
* [CSS](#css)
    * [Bootstrap media query](#bootstrap-media-query)
    * [Custom media query](#custom-media-query)
* [Javascript](#javascript)
    * [Scroll pass element](#scroll-pass-element)
    * [Random positive integer](#random-positive-integer)
* [Analytics]
    * [Setup visibility](#setup-visibility)

## CSS 
### Bootstrap media query
Media queries provided by bootstrap

**variable value**
```css
// xs
max-width: 575.98px
// sm
min-width: 576px and max-width: 767.98px
// md
min-width: 768px and max-width: 991.98px
// lg
min-width: 992px and max-width: 1199.98px
// xl
min-width: 1200px
```
**for any platform bigger than**
```scss
@include media-breakpoint-up(sm) { ... }
@include media-breakpoint-up(md) { ... }
@include media-breakpoint-up(lg) { ... }
@include media-breakpoint-up(xl) { ... }
```
**for any platform smaller than**
```scss
@include media-breakpoint-down(xs) { ... }
@include media-breakpoint-down(sm) { ... }
@include media-breakpoint-down(md) { ... }
@include media-breakpoint-down(lg) { ... }
```
**for any platform in between, eg below between md and xl**
```scss
@include media-breakpoint-between(md, xl) { ... }
```

### Custom media query

**untuk mobile landscape**
```css
@media only screen 
and (max-device-width: 736px) 
and (-webkit-min-device-pixel-ratio: 2)
and (orientation: landscape) { ... }
```

## Javascript

### Scroll pass element

```javascript
window.addEventListener("scroll", function() {
    var targetElement = document.getElementById("targetElement");
    if (window.scrollY > ((targetElement.offsetTop) + (targetElement.offsetHeight))) {
        //when scroll past element do...
    }else{
        //if not do...
    }
}); 
```

### Random positive integer

Random positive integer between max and min number

```javascript
//n is any max number, m is any number less than n and if n - m is not negative
var max = n, min = n - m;
Math.floor(Math.random() * (max - min + 1)) + min;
//result is positive integer between max and min
```

## Analytics

### Setup visibility
Visibility dipakai untuk menentukan apakah sebuah halaman sedang dibuka oleh visitor(Page view). 
Untuk setup visibility dapat dilakukan dengan cara:
* Buka google tag manager
* Buka menu `Tags` > Click `new` 
* Tentukan judul tag
* Pada tag configuration pilih tag type `Google Analytics - Universal analytics`
* Track type pilih `Page view` > Google analytic setting pilih `{{Google analytic setting}}`
* Click triggering, akan terbuka window choose a trigger > click pada icon `+` > akan terbuka window untuk setup trigger
* Beri judul trigger > pada trigger configuration pilih element visibility > isi element id dengan id page 