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

![Animated demo](https://github.com/aquint/ion-alpha-scroll/raw/master/demo.gif)

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
<ion-alpha-scroll ng-model="model" key="keyName" subheader="true">
  Content Goes here...
</ion-alpha-scroll>
```
where 'ng-model' is the model you would like to sort and 'key' is the name of the key you would like to sort by.

The 'subheader' attribute is optional, to be set if using a subheader in the view to allow proper scroll height.

To display the properties of each item in the model, you can use the 'item' object within the directive:
```html
	<ion-alpha-scroll ng-model="model" key="keyName">
	  <div>Name: {{item.name}}</div>
	  <div>Address: {{item.address}}</div>
	</ion-alpha-scroll>
```

Heres a quick example:

services.js
```javascript
angular.module('example.services', [])

.factory('Contacts', function() {

  // Some fake testing data
  var contacts = [
  {
    id: 0,
    name: 'Ben Sparrow',
    address: '123 Fake St.'
    face: 'https://pbs.twimg.com/profile_images/514549811765211136/9SgAuHeY.png'
  }, {
    id: 1,
    name: 'Max Lynx',
    address: '123 Fake St.'
    face: 'https://avatars3.githubusercontent.com/u/11214?v=3&s=460'
  },{
    id: 2,
    name: 'Adam Bradleyson',
    address: '123 Fake St.'
    face: 'https://pbs.twimg.com/profile_images/479090794058379264/84TKj_qa.jpeg'
  }, {
    id: 3,
    name: 'Perry Governor',
    address: '123 Fake St.'
    face: 'https://pbs.twimg.com/profile_images/491995398135767040/ie2Z_V6e.jpeg'
  }, {
    id: 4,
    name: 'Mike Harrington',
    address: '123 Fake St.'
    face: 'https://pbs.twimg.com/profile_images/578237281384841216/R3ae1n61.png'
  }

  ...

  ];


  return {
    all: function() {
      return contacts;
    },
    remove: function(contact) {
      contacts.splice(contacts.indexOf(contact), 1);
    },
    get: function(contactId) {
      for (var i = 0; i < contacts.length; i++) {
        if (contacts[i].id === parseInt(contactId)) {
          return contacts[i];
        }
      }
      return null;
    }
  };
});

```
controllers.js
```javascript
angular.module('example.controllers', [])

.controller('contactsCtrl', ['$scope','Contacts',function($scope, Contacts) {
 
	$scope.contacts = Contacts.all();

)]};

```
contacts-list.html
```html
<ion-view view-title="Contacts">
  <ion-content>
    <ion-alpha-scroll ng-model="contacts" key="name">
      <div>{{item.name}}</div>
      <div>{{item.description}}</div>
    </ion-alpha-scroll>
  </ion-content>
</ion-view>
```

# Acknowledgements

Initial inspiration and code taken from [this codepen](http://codepen.io/mikelucid/pen/mqzLc) by mikelucid

# License

The Ionic alpha-scroll directive is available under the MIT license.
