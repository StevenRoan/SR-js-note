# Module and Dependency Injections


## [Bootstrap](https://docs.angularjs.org/guide/bootstrap)

How to launch(kickstart) an Angular Application
1. **Load** event callback
2. find `ng-app`, or trigger by `angular.bootstrap(DOM[,dep])`
2. Load module, `provider registration` and `configuration phase`
2. get `injector`
2. `Run blocks` of `module` can be thought as `main` function



* Module provide **module** level api

```
angular.module("myModule", []).config(['depProvider', function (depProvider){
//...
})
```

```
angular.module("myModule", []).run(['depService', function (depService){
//...
})
```

## Bootstrap
* `ng-app`
    * By `ng-app`, only **single** angular application can be bootstrapped per HTML document.
* `angular.bootstrap`
    * To run **multiple** applications, use manullay bootstrap
        * **multiple applications** means   




# Two Types of Components

### Controller
* Controller creates a child scope. In html, we use 
```
<ng-controller="first-controller">
```

* `$scope`: Controllers are associated with **an element in the DOM** and so are provided with access to the scope.
* To support minified and uglified code, use `$inject` or inline array [link](https://docs.angularjs.org/guide/di#inline-array-annotation)
* 