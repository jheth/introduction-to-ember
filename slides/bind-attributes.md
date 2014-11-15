## Attribute Binding

```
<img {{bind-attr src=logoUrl}} alt="Logo">

<img src="http://www.example.com/images/logo.png" alt="Logo">
```

```
<input type="checkbox" {{bind-attr disabled=isAdministrator}}>

<input type="checkbox" disabled>
```