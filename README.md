# Catalyst Website Documentation
Documentation for common code used in website development

## Table of content
* [CSS](#css)
    * [Common media query](#common-media-query)
    * [Custom media query](#custom-media-query)
* [Javascript](#javascript)
    * [Scroll pass element](#scroll-pass-element)

## CSS [:arrow_double_up:](#table-of-content) 
### Common media query [:arrow_double_up:](#table-of-content)
Media queries provided in bootstrap

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

### Custom media query [:arrow_double_up:](#table-of-content)

**untuk mobile landscape**
```css
@media only screen 
and (max-device-width: 736px) 
and (-webkit-min-device-pixel-ratio: 2)
and (orientation: landscape) { ... }
```

## Javascript [:arrow_double_up:](#table-of-content)

### Scroll pass element [:arrow_double_up:](#table-of-content)

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