# Priceco style guide

## Install
```js
npm install https://github.com/AdaptRetail/priceco-style
```

## Usage

Import the full style after the `variables`, `mixins` and `functions`.

```sass
@import "node_modules/@priceco/style/src/main.scss";
```

If you need to divide it up you can import section for section.

```sass
@import "node_modules/@priceco/style/src/Utilities/_.scss";
```

### Variables

All the variables are set in `src/style/Utilities/Variables.scss`.
It includes colors, but also `base64` encoded strings of the assets.

An example of this is the `$priceco-logo` variable that contains a base64 string of
![Priceco logo variable](/assets/priceco_logo.svg)

```scss
.logo {
    background: @include background-image( $priceco-logo );
}
```

### Elements

#### Price

##### HTML

![Priceco price tag](/assets/screenshots/price.png)

Make sure there is no space between the price integer and the price decimal. Else there is getting a large space between them.


```html
<div class="price">
    <div class="price__number price__integer">11</div><div class="price__number price__decimal">90</div>
</div>
```

#### Price bomb

Price bombs are elements for get the attention to the price.
This style has two to from.

##### Price match
![Price match](/assets/price-match.png)

```html
<div class="bomb is-pricematch"></div>
```

##### Three for two
![Price match](/assets/three-for-two.png)
```html
<div class="bomb is-threefortwo"></div>
```
