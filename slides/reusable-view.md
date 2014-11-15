##  Reusable View

```
/* {{view "myText" value=name inputDidChange=nameDidChange}} */
App.MyText = Ember.TextField.extend({
  inputDidChange: false,
  change: function() {
    this.set('inputDidChange', true);
  }
});
```

