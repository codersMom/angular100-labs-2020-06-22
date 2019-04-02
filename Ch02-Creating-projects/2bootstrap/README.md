npm install bootstrap -S

Modify angular-cli.json to add bootstrap

```json
"styles": [
  "./node_modules/bootstrap/dist/css/bootstrap.min.css",
  "src/styles.css"
]
```

Modify appcompoent to have jumbotron etc

```html
<div style="text-align:center;">
  <h1 class="jumbotron my-5 mx-5">
    Welcome to {{ title }}!
  </h1>
</div>
```
