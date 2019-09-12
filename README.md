# angularjs-intl-tel-input

### Demo

https://rc125.github.io/angularjs-intl-tel-input/

## Getting Started
1. Download the [latest release](https://github.com/jackocnr/intl-tel-input/releases/latest), or better yet install it with [npm](https://www.npmjs.com/package/intl-tel-input)

2. Include the stylesheet
  ```html
  <link rel="stylesheet" href="path/to/intlTelInput.css">
  ```

3. Override the path to flags.png in your CSS
  ```css
  .iti__flag {background-image: url("path/to/flags.png");}

  @media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
    .iti__flag {background-image: url("path/to/flags@2x.png");}
  }
  ```

4. Add the plugin script and initialise it on your input element
  ```html
  <input type="tel" id="phone">

  <script src="path/to/intlTelInput.js"></script>
  <script>
    var input = document.querySelector("#phone");
    window.intlTelInput(input);
  </script>
  ```

5. **Recommended:** initialise the plugin with the `utilsScript` option to enable formatting/validation, and to allow you to extract full international numbers using `getNumber`.

### Setup and config

Inject `ngIntlTelInput` into your application module

```javascript
var myApp = angular.module('myApp', ['ngIntlTelInput']);
```

### Config

Configure defaults

> See: https://github.com/Bluefieldscom/intl-tel-input#options

```javascript
angular.module('myApp')
  .config(function (ngIntlTelInputProvider) {
    ngIntlTelInputProvider.set({initialCountry: 'us'});
  });
```

### Usage

#### ng-intl-tel-input attribute

This attribute applies _intl-tel-input_ to a **text** field.

```html
<input type="text" ng-model="model.tel" ng-intl-tel-input>
```

**Note**

* `type` is set to *text* or *tel*
* `ng-model` is specified (required)

#### data-default-country attribute

This attribute allows run-time setting of the default country.

```html
<input type="text" ng-model="model.tel" ng-intl-tel-input data-initial-country="gb">
```
