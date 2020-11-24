# Thing

UI patterns and components for reuse across Subvisual Design Systems
[Live components](https://codepen.io/azevedo-252/pens/tags/?grid_type=list&selected_tag=thing)

* [HTML5 doctype](#html5-doctype)
* [Scss](#scss)
  * [Settings](#settings)
  * [Tools](#tools)
  * [Generic](#generic)
  * [Components](#components)
  * [Utilites](#utilities)

## HTML5 doctype

Most HTML elements and CSS properties require the use of the HTML5 doctype.
Include it at the beginning of all your pages.

index.html
```html
<!doctype html>
<html lang="en">
  ...
</html>
```

## SCSS

**Dependencies**:

* https://github.com/eduardoboucas/include-media

[index.scss](scss/index.scss)
```scss
// If using webpack and any special configuration for webpack;
// Otherwise import the lib according to your build tools
@import "~include-media/dist/include-media";

// Settings
@import "./colors";
@import "./sizes";
@import "./typography";
@import "./other";

// Tools
@import "./mixins";

// Generic
@import "./reset";
@import "./normalize";
@import "./box_sizing";

// Components
@import "./components/index";

// Utilites
@import "./utilities";
```

### Settings

<details>
  <summary>Colors</summary>

  _colors.scss
  ```scss
  $light-navy-blue: #2a567c;
  $white: #fff;
  ```
</details>

<details>
  <summary>Sizes</summary>

  _sizes.scss
  ```scss
  $size-xxxxsmall: 4px;
  $size-xxxsmall: 8px;
  $size-xxsmall: 12px;
  $size-xsmall: 16px;
  $size-small: 20px;
  $size-base: 28px;
  $size-large: 40px;
  $size-xlarge: 56px;
  $size-xxlarge: 80px;
  $size-xxxlarge: 112px;
  $size-xxxxlarge: 160px;
  ```
</details>

<details>
  <summary>Typography</summary>

  _typography.scss
  ```scss
  $font-family-sans: "sofia-pro", helvetica arial, sans-serif;
  $font-weight-light: 300;
  $font-weight-regular: 400;
  $font-weight-bold: 700;
  ```
</details>

<details>
  <summary>Other</summary>

  _other.scss
  ```scss
  $layer-overlay: 8000;
  $layer-modal: 9000;

  // For include-media
  $breakpoints: (small: 600px, large: 1280px);
  ```
</details>

### Tools

<details>
  <summary>Mixins</summary>

  _mixins.scss
  ```scss
  @mixin VisuallyHidden {
    position: absolute;

    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;

    border: 0;
    clip: rect(0 0 0 0);
  }


  @mixin GridContainer {
    display: grid;
    width: 100%;
    max-width: 1107px;
    grid-template-columns: repeat(9, minmax(0, 103px));
    grid-column-gap: $size-xsmall;

    @include media(">small") {
      grid-column-gap: $size-small;
    }

    @include media(">large") {
      grid-column-gap: $size-base;
    }
  }

  @mixin Placeholder {
    &::-webkit-input-placeholder {
      @content;
    }
    &::-moz-placeholder {
      @content;
    }
    &:-ms-input-placeholder {
      @content;
    }
    &:-moz-placeholder {
      @content;
    }
  }
  ```
</details>

### Generic

<details>
  <summary>Reset</summary>

  _reset.scss
  ```scss
  /* http://meyerweb.com/eric/tools/css/reset/
     v2.0 | 20110126
     License: none (public domain)
  */

  html, body, div, span, applet, object, iframe,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  a, abbr, acronym, address, big, cite, code,
  del, dfn, em, img, ins, kbd, q, s, samp,
  small, strike, strong, sub, sup, tt, var,
  b, u, i, center,
  dl, dt, dd, ol, ul, li,
  fieldset, form, label, legend,
  table, caption, tbody, tfoot, thead, tr, th, td,
  article, aside, canvas, details, embed,
  figure, figcaption, footer, header, hgroup,
  menu, nav, output, ruby, section, summary,
  time, mark, audio, video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
  }
  /* HTML5 display-role reset for older browsers */
  article, aside, details, figcaption, figure,
  footer, header, hgroup, menu, nav, section {
    display: block;
  }
  body {
    line-height: 1;
  }
  ol, ul {
    list-style: none;
  }
  blockquote, q {
    quotes: none;
  }
  blockquote:before, blockquote:after,
  q:before, q:after {
    content: '';
    content: none;
  }
  table {
    border-collapse: collapse;
    border-spacing: 0;
  }
  button {
    padding: 0;
    border: 0;
  }
  ```
</details>

<details>
  <summary>Normalize</summary>

  _normalize.scss
  ```scss
  html,
  body {
    height: 100%;

    background: $white;
    color: $light-navy-blue;

    font-family: $font-family-sans;
    font-size: $size-small;
    line-height: $size-base;

    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: auto;
    text-rendering: optimizeLegibility;
  }
  ```
</details>

<details>
  <summary>Box Sizing</summary>

  _box_sizing.scss
  ```scss
  html {
    box-sizing: border-box;
  }

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  ```
</details>

### Components

### Utilites

_utilities.scss
```scss
```
