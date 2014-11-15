##  Controller

A controller is an object that stores application state.

```
App.PostsController = Ember.ArrayController.extend({
  /* Computed Property */
  publishedCount: function() {
    return this.get('model').filterBy('isPublished', true).get('length');
  }.property('model.@each.isPublished'),

  /* Observer */
  monitorPosts: function() {
    console.log('Posts Array Changed');
  }.observes('model'),

  /* Respond to Actions */
  actions {
    save: function(post) {
      this.get('model').addObject(post);
    }
  }
});
```

Note:

A template can optionally have a controller in addition to a model, and can retrieve properties from both.