##  Templates
http://handlebarsjs.com/

Templates describes the user interface of your application.

```
<div class="entry">
  <h1>{{title}}</h1>
  <div class="body">
    {{body}}
  </div>
</div>
```

```
<ul>
  {{#each people}}
    <li>{{name}}</li>
  {{/each}}
</ul>
```

```
{{#if person}}
  Welcome back, <b>{{person.firstName}} {{person.lastName}}</b>!
{{else}}
  Please log in.
{{/if}}
```

Note:
Standalone templating language that Ember depends on and enhances the functionality.

Handlebars templates look like regular HTML, with embedded handlebars expressions.

You can deliver a template to the browser by including it in a script tag.