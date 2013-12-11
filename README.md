# angular-pickadate

A simple and fluid inline datepicker for AngularJS with no extra dependencies.

![pickadate](http://img.ctrlv.in/img/5294e96436552.jpg)

### Demo

<a href="http://embed.plnkr.co/gXP8xdsdP9nJIr0fi1RQ/preview" target="_blank">View demo in a new window</a>

### Installation

1) Add the `pickadate` module to your dependencies

```javascript
angular.module('myApp', ['pickadate']);
```

2) Use the `pickadate` directive in any element

```html
<div pickadate ng-model="date"></div>
```

Pickadate is fluid, so it will take the width of the parent container.

### Pickadate options

#### min-date, max-date

```html
<div pickadate ng-model="date" min-date="minDate" max-date="maxDate"></div>
```

```javascript
function MyAppController($scope) {
    $scope.minDate = '2013-11-10';
    $scope.maxDate = '2013-12-31';
}
```

`min-date` and `max-date` take angluar expressions, so if you want to specify the values inline, don't forget the quotes!

```html
<div pickadate ng-model="date" min-date="'2013-11-10'" max-date="'2013-12-31'"></div>
```

#### disabled-dates

```html
<div pickadate ng-model="date" disabled-dates="disabledDates"></div>
```

```javascript
function MyAppController($scope) {
    $scope.disabledDates = ['2013-11-10', '2013-11-15', '2013-11-19'];
}
```

### I18n

Pickadate uses angular `$locale` module. If you want to have the calendar in any other language, please include the corresponding AngularJS i18n files. You can get them here: [http://code.angularjs.org/1.2.0-rc.2/i18n/](http://code.angularjs.org/1.2.0-rc.2/i18n/)


### Future development

Currently `pickadate` only works as an inline datepicker, but would like it to make it work in any text input as an overlay like the `jquery-ui` one. Will be happy to merge your pull requests.

