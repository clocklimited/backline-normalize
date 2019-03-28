# Backline Normalize

Based on [normalize.css](http://necolas.github.io/normalize.css/), but with some more opinionated additions.

## Installation

```sh
npm install --save backline-normalize
```

or

```sh
yarn add backline-normalize
```

Add `backline-normalize` to your node-sass includePaths option.

```js
{
  loader: 'sass-loader',
  options: {
    includePaths: [
      ...require('backline-normalize').includePaths
    ]
  }
}
```

Import backline-normalize in each `.scss` as required

```scss
@import 'backline-normalize';
```

---

## Opinionated additions

### Change the default box-sizing

Uses `box-sizing: border-box` on the `html` element, then `box-sizing: inherit` for all other elements.

[Reference: CSS Tricks](https://css-tricks.com/inheriting-box-sizing-probably-slightly-better-best-practice/)

### Remove all margin/padding

This allows elements to provide their own unique spacing, or for containers to space their child elements as required.

### Un-style all headings

Detaches the semantics of the heading elements from how they look.

### Un-style buttons

Removes the default `background`, `border` and `border-radius`. The result looks morelike an anchor element and is an easier starting point point for adding custom styles.

### Make images responsive by default

Images appear at their natural size by default, but scale down if their container is narrower.

### Make small larger

Resets `<small>` to look like regular text. The semantics of `<small>` have moved away from just looking visually small, to now “represent side-comments and small print, including copyright and legal text, independent of its styled presentation”.

[Reference: W3C](http://w3c.github.io/html-reference/small.html)
