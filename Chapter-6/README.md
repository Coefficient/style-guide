# AngularJS Style Guide

##### Some links

> - [Opinionated Angular](https://medium.com/opinionated-angularjs/9f01b594bf06)

- We are using the following design pattern for angular modules.

```javascript
(function() {
    'use strict';

    var moduleName = 'app.foo.bar',

        angularDependencies = [
            'ui.router'
        ];

    define([
        'angular',
        'ui.router'
    ], function(angular) {

        var module = angular.module(moduleName, angularDependencies);

        return module;
    });
})();
```
- A state will look like this

```javascript
module.config(['$stateProvider',
    function($stateProvider) {

        $stateProvider.state('app.foo.bar', {
            controller: 'fooCtrl',
            url: '/foo',
            templateUrl: 'foo/_foo.html'
        });
    }
]);
```
- A controller will look like this. Bump the `function` to the next line and indent it to maintain readability. Sometimes the dependencies will get fairly long.

```javascript
module.controller('fooCtrl', ['$scope', '$state',
    function($scope, $state) {
        console.log('fooCtrl');
    }
]);
```
- When writing promises that have a `success` and an `error` callback, they should be written like this for readability.

```javascript
$q.all(arrayOfRequests).then(
    function success(response) {
        // success stuff
    },
    function error(response) {
        // error stuff
    }
);
```

- HTML that contains directives, should have some sort of order, generally speaking, try and put all the directives at the end of the tag, after basic HTML attributes.

`<div class="foo bar" title="something" ng-click="clickThing()"></div>`

<table><tr><td><a href="../Chapter-5/README.md">&larr; Previous</a></td><td><a href="../Chapter-7/README.md">Next &rarr;</a></td></tr></table>
