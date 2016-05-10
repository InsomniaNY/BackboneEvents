# BackboneEvents

#### Summary
Allows access to Backbone.Events on, off, and trigger functions without the need for Backbone.js itself or all the other fluff



#### Description
  Extracted from **Backbone.js 1.3.3**
  
  This allows the use of Backbone.Events without having to load the entirety of Backbone.
  
  Reason: The Backbone.Events system is more versatile than jQuery Custom Events and this
          provides a smaller footprint than loading the entire Backbone.js file or the
          unnecessary functions listed below.
  
  Functions Included: on, off, trigger
  
  Functions _NOT_ Included: listenTo, stopListening, once, listenToOnce




#### Example
###### Set Global Variable to extend Backbone.Events:
```
var myEvents = _.extend({}, Backbone.Events);
```

###### Without Data:
```
myEvents.trigger('myevent');

myEvents.on('myevent', function(){
    // When myevent is triggered, execute this code
});
```

###### With Data:
```
myEvents.trigger('myevent', data);

myEvents.on('myevent', function(data){
    // When myevent is triggered, execute this code
});
```