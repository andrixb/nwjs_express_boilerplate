# NWJS package express app

## Option 1 

Clone the repo 

```
npm install
```

```
npm start
```

This is what you should see. 

[Express example app](./img/express_example.png)

And modify express app accordingly. 

---

## Option 2 

Don't clone the repo, and follow these inscructions from terminal 

- Setup express
- setup nwjs
- `package.json` 
- `index.html`

### Setup express 

express generator
```
npm install express-generator
```

boilerplate for express

```
express
```

### Setup nwjs 

Install nw js locally

```
npm install --save nw
```


### modify `package.json` for nwjs 

```json
{
  "name": "autoedit_nwjs",
  "version": "0.0.0",
  "node-main": "./bin/www",
  "main" : "index.html",
  "window": {
    "toolbar": true,
    "width": 800,
    "height": 600
  },
  "private": true,
  "scripts": {
    "start": "nw"
  },
  "dependencies": {
    "body-parser": "~1.13.2",
    "cookie-parser": "~1.3.5",
    "debug": "~2.2.0",
    "express": "~4.13.1",
    "jade": "~1.11.0",
    "morgan": "~1.6.1",
    "nw": "^0.12.3",
    "serve-favicon": "~2.3.0"
  }
}
```


### make `index.html`for nwjs 

Calling ` location.href="http://localhost:3000"` when DOM is ready to load express from server

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Test</title>

</head>
<body>
  <script type="text/javascript">

  document.addEventListener("DOMContentLoaded", function(){
    location.href="http://localhost:3000";
  });

  </script>

</body>
</html>
```

----

## mongodb?
Next up, how to package mongodb in NWJS app?