ion-alpha-scroll
================

> Configurable Ionic directive for alphabetically indexed list with an alpha scroll bar.

#Table of contents

- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgements](#acknowledgements)
- [License](#license)

# Demo

![Animated demo](https://github.com/aquint/ion-alpha-scroll/raw/master/demo.webm)

# Installation

1. Use bower to install the new module:
```bash
bower install ion-alpha-scroll --save
```
2. Import the `ion-alpha-scroll` javascript and css file into your HTML file:
```html
<script src="bower_components/ion-alpha-scroll/dist/ion-alpha-scroll.js"></script>
<link href="bower_components/ion-alpha-scroll/dist/ion-alpha-scroll.css" rel="stylesheet">
```
3. Add `ion-alpha-scroll` as a dependency on your Ionic app:
```javascript
angular.module('myApp', [
  'ionic',
  'ion-alpha-scroll'
]);
```

# Usage

To use the `ion-alpha-scroll` directive simply add the following snippet to your template:
```html
<ion-alpha-scroll ng-model="model" key="keyName">
  Content Goes here...
</ion-alpha-scroll>
```
where 'ng-model' is the model you would like to sort and 'key' is the name of the key you would like to sort by.

Heres a quick example:

```javascript
$scope.callbackMethod = function (query) {
    return [query];
}
```


# Acknowledgements

Initial inspiration and code taken from [this codepen](http://codepen.io/mikelucid/pen/mqzLc) by mikelucid

# License

The Ionic alpha-scroll directive is available under the MIT license.
