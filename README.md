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

The library exposes three functions:
```js
function createAlert(title, body, mode, callback, callbackLabel)
```
Here,
* `title` is the title that will be displayed in the alert header
* `body` is an HTML string that will be displayed in the alert body
* `mode` is a string parameter. If `mode === 'error'`, the alert will be displayed with the close button hidden.
* `callback` is a reference to a function. If this reference is valid, a second button will be displayed that will execute the function when clicked.
* `callbackLabel` is a label for the callback button.
This function creates a generic message box.

```js
function createPrompt(title, msg, callback, callbackLabel, onErr)
```
Here,
* `title` is the title that will be displayed in the prompt header.
* `msg` is a string that will be displayed in the prompt body next to a text field.
* `callback` is a reference to a function. If this reference is valid, a second button will be displayed that will execute the function when clicked.
* `callbackLabel` is a label for the callback button.

This function creates a prompt dialog. The prompt takes a callback as an argument, to which the user-entered string is passed. Incase the user cancels the input or enters an empty string,  the onErr function is called with either the parameter `ALERT_EMPTY_FIELD` or `ALERT_CANCELLED`.

```js
function createConfirm(title, msg, yes, no, yesLabel, noLabel)
```
Here,
* `title` is the title that will be displayed in the dialog header.
* `msg` is a string that will be displayed in the dialog body next to a text field.
* `yes` and `no` are references to functions. The functions are called when the user clicks the yes or no button respectively.
* `yesLabel` and `noLabel` are labels for the `yes` and `no` buttons respectively.

This function creates a prompt dialog, using callbacks for confirm / cancel actions.

```js
function hideAlert()
```
Calling hideAlert() will simply hide the alert.

### Contributing
Fork the repo and make a PR.

---

Copyright © 2021 Siddharth Singh