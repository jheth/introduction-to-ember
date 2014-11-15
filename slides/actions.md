##  Actions

```
{{#if isExpanded}}
  <div class='body'>{{body}}</div>
  <button {{action 'contract'}}>Contract</button>
{{else}}
  <button {{action 'expand'}}>Show More...</button>
{{/if}}
```

```
App.PostController = Ember.ObjectController.extend({
  // initial value
  isExpanded: false,

  actions: {
    expand: function() {
      this.set('isExpanded', true);
      return true; // Bubble up the chain.
    },

    contract: function() {
      this.set('isExpanded', false);
      return false; // Prevents bubbling.
    }
  }
});
```

Note:
{{action}} helper makes an HTML element clickable
Named event it sent to your application
Bubbling occurs with returning true or false.