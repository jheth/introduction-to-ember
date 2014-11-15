##  Component

```
<!-- blog-post.hbs {{blog-post post=object}} -->
<h1>{{post.title}}</h1>
<div class="post">
  {{#if isEditing}}
    {{textarea value=post.body}}
    <button {{action 'save'}}>Save</button>
  {{else}}
    {{post.body}}
    <button {{action 'edit'}}>Edit</button>
  {{/if}}
</div>
```

```
App.BlogPostComponent = Ember.Component.extend({
  tagName: 'div',
  isEditing: false,
  actions: {
    edit: function() {
      this.set('isEditing', true);
    },
    save: function() {
      this.set('isEditing', false);
    }
  }
});
```

Note:

An Ember.Component is a view that is completely isolated. Property access in its templates go to the view object and actions are targeted at the view object. There is no access to the surrounding context or outer controller; all contextual information must be passed in.

A component is a custom HTML tag whose behavior you implement using JavaScript and whose appearance you describe using Handlebars templates. They allow you to create reusable controls that can simplify your application's templates.