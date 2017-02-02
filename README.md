# pjax-component

A [Custom Element](https://developers.google.com/web/fundamentals/getting-started/primers/customelements) that PJAXs its content.

## Install

```sh
$ npm i pjax-component --save
```

## Use

Decide on a `name` for your element (it must contain a `-`).

Using your `name`, add the new element(s) to your HTML:

```html
<!-- dont forget the closing tag -->
<pjax-component content="path/to/html" fetch="false"></pjax-component>
```

Then, in your JavaScript, pass your `name` to the import:

```javascript
// import the package
import createPJAXComponent from 'pjax-component'

// call the imported function
// pass your element name as used in the HTML
createPJAXComponent('pjax-component')
```

When you're ready for the element to PJAX its content, change the `fetch` attribute to `true`.

```javascript
document
  .getElementById('component')
  .setAttribute('fetch', true)
```

## License

[MIT](https://opensource.org/licenses/MIT). © 2017 Michael Cavalea
