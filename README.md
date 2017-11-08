![Priceco logo](/assets/priceco_logo.svg)
# Style guide and HTML elements

This repository contains extracted style elements for templates for a demo client in [Adapt Retail](https://adaptretail.com).
We use this style in the following productions.
- [Banner template](https://github.com/AdaptRetail/banner-template)
- [Print template](https://github.com/AdaptRetail/print-template)
- [Video template](https://github.com/AdaptRetail/video-template)

The purpose is to minimize the code you need to write for each project.
When you have extracted the code, you can change it one place, and others get automatically updated.

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

### Utilities

Contains the variables.

```sass
@import "node_modules/@priceco/style/src/Utilities/_all.scss";
```

### Elements

Import after the `mixins` and the `functions`.

```sass
@import "node_modules/@priceco/style/src/Utilities/_all.scss";
```

### Variables

All Sass the variables are set in `src/style/Utilities/Variables.scss`.

#### Colors

Priceco main colors.

- `$priceco-blue`
- `$priceco-red`
- `$priceco-yellow`
- `$priceco-blue-gradient`

#### Images

Contains `base64` encoded strings of the image assets.

- `$priceco-logo`
- `$priceco-price-bg`
- `$priceco-price-match`
- `$priceco-three-for-two`

An example of this is the `$priceco-logo` variable that contains a base64 string of the priceco logo.

```scss
.logo {
    background: @include background-image( $priceco-logo );
}
```

### Elements

The elements are built on a super responsive way, so it can be used in both print productions and responsive web banners in [Adapt Retail](https://adaptretail.com).

#### Price

##### HTML

![Priceco price tag](/assets/screenshots/price.png)

> Make sure there is no space between the `price integer` and the `price decimal`.
> Else there is getting a large space between them.

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
