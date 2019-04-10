# CatalystDocuments
Documentation for common code used in website development

## Common media query
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
**for any platform that bigger than**
```scss
    @include media-breakpoint-up(sm) { ... }
    @include media-breakpoint-up(md) { ... }
    @include media-breakpoint-up(lg) { ... }
    @include media-breakpoint-up(xl) { ... }
```
**for any platform that smaller than**
```scss
    @include media-breakpoint-down(xs) { ... }
    @include media-breakpoint-down(sm) { ... }
    @include media-breakpoint-down(md) { ... }
    @include media-breakpoint-down(lg) { ... }
```
**for any platform in between, eg below between md and xl**
```css
    @include media-breakpoint-between(md, xl) { ... }
```

## Custom media query

**untuk mobile landscape**
```css
    @media only screen 
    and (max-device-width: 736px) 
    and (-webkit-min-device-pixel-ratio: 2)
    and (orientation: landscape) {...}
```