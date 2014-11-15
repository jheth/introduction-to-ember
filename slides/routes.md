##  Routes

A route is an object that tells the template which model it should display.

```
App.PostsRoute = Ember.Route.extend({
  beforeModel: function(transition) { },
  model: function() {
    // return jQuery.getJSON("/posts");
    // return this.store.find('posts');
    return [{
      id: 1,
      title: "Ember.js",
      body: "This is a sample blog post"
    }, {
      id: 2,
      title: "Eiffel Tower",
      body: "This has information about the Eiffel Tower"
    }];
  },
  afterModel: function(model, transition) { }
});
```