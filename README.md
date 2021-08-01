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
- [Icon Moon](https://icomoon.io/)


## Node Sass Compile

```json
{
  "name": "natours",
  "version": "1.0.0",
  "description": "Landing page for natours",
  "main": "index.js",
  "scripts": {
    "watch:sass": "node-sass sass/main.scss css/style.css -w",
    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
  },
  "author": "Jonas",
  "license": "ISC",
  "devDependencies": {
    "autoprefixer": "^7.1.4",
    "concat": "^1.0.3",
    "node-sass": "^4.5.3",
    "npm-run-all": "^4.1.1",
    "postcss-cli": "^4.1.1"
  }
}
```