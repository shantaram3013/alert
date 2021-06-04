# alert

A vanilla JS/CSS in-page dialog implementation.

### Usage

#### Adding to your project

Include it in your page by adding the stylesheet to the `<head>` of your page:
```html
<link rel='stylesheet' href='alert.css'>
```
And the JS source at the bottom of the `<body>` of your page:
```html
<script src='alert.js'>
```

#### API

The library exposes only two functions:
```js
function createAlert(title, body, mode, callback, callbackLabel)
```
Here,
* `title` is the title that will be displayed in the alert header
* `body` is an HTML string that will be displayed in the alert body
* `mode` is a string parameter. If `mode === 'error'`, the alert will be displayed with the close button hidden.
* `callback` is a reference to a function. If this reference is valid, a second button will be displayed that will execute the function when clicked.
* `callbackLabel` is a label for the callback button.

```js
function hideAlert()
```
Calling hideAlert() will simply hide the alert.

### Contributing
Fork the repo and make a PR.

---

Copyright © 2021 Siddharth Singh