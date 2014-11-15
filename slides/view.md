##  View

Responsible for responding to user interactions.

```
App.PostView = Ember.View.extend({
  click: function() {
    // Respond to click events
    this.get('controller').send('actionName');
  },
  didInsertElement: function() {
    // Perform logic when element is inserted into the DOM
  },
  willDestroyElement: function() {
    // Perform logic before element is removed into the DOM
  }
});
```

Note:
Views like Routes have lifecycles to them.

The view is responsible for turning a primitive event (a click) into a semantic event: delete this todo! These semantic events are first sent up to the controller, or if no method is defined there, your application's router, which is responsible for reacting to the event based on the current state of the application.