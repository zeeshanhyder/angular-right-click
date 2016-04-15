# angular-right-click
Angular right click and context menu library. No dependencies.

## Installation

### General
- Copy/move `ng-right-click.js` from `src` dir in the package to your project dir
- In your Angular app, add a dependency to your module as below:
  
  `angular.module('yourApp',['ngRightClick',...]');` 
  
### bower

In your project dir, type the following command:

```sh
$ bower install angular-right-click
```
Then add a `<script>` in your project `html`:

```javascript
<script src='/bower_components/angular-right-click/src/ng-right-click.js'></script>
```
And finally in your Angular app, add the dependency as:

`angular.module('yourApp',['ngRightClick',...]');`

### npm
In your project dir, run the following command:

```sh
$ npm install angular-right-click
```
Then `require()` in your project source as:

```javascript
require('angular-right-click')
```

### CSS 
Import default `css` file in your project `index` file as: 

```html
<link rel="stylesheet" href="[node_modules | bower_components]/angular-right-click/src/css/ng-right-click.css">
```

## Usage

### Basic callback only (like `ng-click`, no context menu)

```html
<div ng-right-click="someFunction()"></div>
```

### Context-menu only option

In your html file, use the component like this:

```html
<div ng-right-click menu-items="menuItems"></div>
```

### Both callback and context-menu option

```html
<div ng-right-click="someFunction()" menu-items="menuItems"></div>
```

where the data format is (in your controller):

```javascript
$scope.sayHello = function(){
    //say hello!
};

$scope.menuItems = [
      { text: "Menu Item 1", //menu option text
        disabled: true //No click event. Grayed out option.
      },
      {
        text:"Menu Item 2", 
        callback: sayHello, //function to be called on click 
        disabled: false
      }
    ];
```

### Styling

I have included a default `css` file for default styling. Include it in your file. You can easily override it with your custom `css` class lie that:

```html
<div ng-right-click menu-items="menuItems" menu-class="custom-css-class"></div>
```

## Examples

Please check the examples directory to get the gist!

Check code example [here](https://github.com/zeeshanhyder/angular-right-click/tree/master/examples).
