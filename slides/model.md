##  Model

A model is an object that stores persistent state.

```javascript
/* Ember Data Model */
App.Post = DS.Model.extend({
  title: DS.attr('string'),
  body: DS.attr('string'),
  author: DS.attr('string'),
  isPublished: DS.attr('date'),
  createdAt: DS.attr('boolean')
});
```

Note:

Templates are responsible for displaying the model to the user by turning it into HTML.
In many applications, models are loaded via an HTTP JSON API, although Ember is agnostic to the backend that you choose.