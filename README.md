# angularjs-intl-tel-input

### Demo

https://rc125.github.io/angularjs-intl-tel-input/

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
