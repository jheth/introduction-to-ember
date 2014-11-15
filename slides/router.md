##  Router

```
App.Router.map(function() {
  this.route("about", { path: "/about" });
  this.route('posts');
  this.route('post', { path: '/post/:post_id' });
});
```

Manages Application State

Deep Linking

Note:
The router translates a URL into a series of nested templates, each backed by a model. As the templates or models being shown to the user change, Ember automatically keeps the URL in the browser's address bar up-to-date.

This means that, at any point, users are able to share the URL of your app. When someone clicks the link, they reliably see the same content as the original user.