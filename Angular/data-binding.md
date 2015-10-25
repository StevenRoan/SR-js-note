# Data Binding

* Use `{{data}}` in the html achieve two-way data binding, **Angular** create a watcher as following in the js.

```
$scope.$watch('data'. function (n, o) {
  //related action
})
```

## `$digest` Cycle
Angular `$digest` cycle check if all the **watched**,`$scope.$watch` data is changed or not.

### When does `$digest` being executed
 * **Navigation events**: Users clicking on links, using back and forward buttons,
and so on.

* **Network events**: All the calls to the `$http` service (and resources created
with $resource ) will trigger a `$digest loop` when a response (either success
or error) is ready.

* **DOM events**: All the AngularJS directives corresponding to DOM events
( ng-click , ng-mouseover , and so on) will trigger a $digest loop when an
event handler is firing.

* **JavaScript timers**: The `$timeout` service wraps the JavaScript setTimeout
function and will trigger a `$digest` loop when a timer fires.


## Difference between `$digest` and `$apply`

* `$digest` works on childScope and `$apply`, if called without argument, works on **rootScope**


## `ng-bind` VS `ng-model`
`ng-bind` is one way data binding, and `ng-model` is two way, which means **view -> model**.


# Bind only once
`<p>Name: {{::name}}</p>`, this usage only bind once and add no watcher ad all.