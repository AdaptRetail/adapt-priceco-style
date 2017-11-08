# Priceco style guide

## Install
```js
npm install https://github.com/AdaptRetail/priceco-style
```

## Usage

Import the style after the `variables`, `mixins` and `functions`.

```sass
@import "node_modules/@priceco/style/src/main.scss";
```

## Elements

### Price

#### HTML

IMAGE

Make sure there is no space between the price integer and the price decimal. Else there is getting a large space between them.


```html
<div class="price">
    <div class="price__number price__integer">11</div><div class="price__number price__decimal">90</div>
</div>
```

### Bomb

IMAGE

#### HTML
```html
<!-- Price match bomb/tag -->
<div class="bomb is-pricematch"></div>

<!-- Three for two bomb/tag -->
<div class="bomb is-threefortwo"></div>
```
