# Advanced CSS and Sass: FlexBox, Grid, Animations and More

---

## Three Pillars of Good HTML and CSS

- Responsive Design:
  - fluid layouts
  - media queries
  - responsive images
  - correct units
  - desktop-first vs mobile-first
- Maintainable and scale code:
  - Clean
  - Easy-to-understand
  - Growth
  - Reusable
  - how to organize files
  - how to name classes
  - how to structure html
- Web Performance:
  - Less HTTP Requests
  - less code
  - Compress Code
  - use a css preprocessor
  - less images
  - compress images

## Some selectors

```css
.button {
}
nav#nav div.pull-right .button {
}
a {
}
#nav a.button:hove {
}
```

```sass

@mixin clearfix {
  &::after {
    content: '';
    clear: both;
    display: table;
  }
}
@mixin style-link-text($color) {
  text-decoration: none;
  text-transform: uppercase;
  color: $color;
}
nav {
    @include clearfix;
    @include style-link-text(blue);
}

```

## Links

- [Images](https://unsplash.com/s/photos/snap)
- [Videos](https://coverr.co)
