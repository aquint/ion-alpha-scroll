ion-autocomplete
================

> Configurable Ionic directive for alphabetically indexed list with an alpha scroll bar.

#Table of contents

- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgements](#acknowledgements)
- [License](#license)

# Demo

![Animated demo](https://github.com/aquint/ion-alpha-scroll/raw/master/demo.gif)

# Installation

1. Use bower to install the new module:
```bash
bower install ion-autocomplete --save
```
2. Import the `ion-autocomplete` javascript and css file into your HTML file:
```html
<script src="bower_components/ion-autocomplete/dist/ion-autocomplete.js"></script>
<link href="bower_components/ion-autocomplete/dist/ion-autocomplete.css" rel="stylesheet">
```
3. Add `ion-autocomplete` as a dependency on your Ionic app:
```javascript
angular.module('myApp', [
  'ionic',
  'ion-autocomplete'
]);
```

# Usage

To use the `ion-autocomplete` directive in single select mode you need to add the following snippet to your template:
```html
<ion-autocomplete ng-model="model" />
```

If you want to use it in multiple select mode you need to add the following snippet to your template: 
```html
<ion-autocomplete ng-model="model" multiple-select="true" />
```

Check out the next chapter on how to configure the directive.

```javascript
$scope.callbackMethod = function (query) {
    return [query];
}
```


# Acknowledgements

Initial inspiration and code taken from [this codepen](http://codepen.io/mikelucid/pen/mqzLc) by mikelucid

# License

This Ionic alpha-scroll directive is available under the MIT license.
