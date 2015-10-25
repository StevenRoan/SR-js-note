## Router
* stream-router.js [src](https://github.com/GoogleCloudPlatform/gcloud-node/blob/584adb51a8506b0e97c2f4810a05ae96318af224/lib/common/stream-router.js#L54). This function adds a middleware (中介層) like before all class method invocation. *We can think* this function acts as a method override.


```
streamRouter.extend = function(Class, methodNames) {
  methodNames = arrify(methodNames);

  methodNames.forEach(function(methodName) {
    var originalMethod = Class.prototype[methodName];

    Class.prototype[methodName] = function() {
      var parsedArguments = streamRouter.parseArguments_(arguments);
      return streamRouter.router_(parsedArguments, originalMethod.bind(this));
    };
  });
};