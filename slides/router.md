##  Router

```javascript
// Manages Application State
// Allows Deep Linking
App.Router.map(function() {
  this.route("about", { path: "/about" });
  this.route('posts');
  this.resource('post', { path: '/post/:post_id' }, function () {
    this.route('edit');
  });
});
```

| URL | Route Name  | Controller | Route | Template |
| - | - | - | - | - |
| /about | about | AboutController | AboutRoute | about.hbs |
| /posts | posts | PostsController | PostsRoute | posts.hbs |
| /post/:post_id | post.index | PostIndexController | PostIndexRoute | posts/index.hbs |
| /post/:post_id/edit | post.edit | PostEditController | PostEditRoute | posts/edit.hbs |

Note:
The router translates a URL into a series of nested templates, each backed by a model. As the templates or models being shown to the user change, Ember automatically keeps the URL in the browser's address bar up-to-date.

This means that, at any point, users are able to share the URL of your app. When someone clicks the link, they reliably see the same content as the original user.