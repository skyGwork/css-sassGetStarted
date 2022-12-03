npm

```JSON
//   TYPE-01

  "scripts": {
    "go-live": "set PORT=9000 && live-server",
    "watch-sass": "sass --watch sass/main.scss src/css/main.css",
    "concat-css": "concat -o src/css/concat.css src/css/main.css src/demo1.css src/demo2.css ",
    "prefix-css": "postcss --use autoprefixer -b 'last 10 versions' src/css/concat.css -o src/css/main.css"
  },

//   TYPE-02

  "scripts": {
    "watch-sass": "sass --watch sass/main.scss css/style.css",
    "devserver": "live-server --browser=firefox",
    "start": "npm-run-all --parallel devserver watch-sass",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.comp.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build:css": "npm-run-all compile:sass prefix:css compress:css"
  },

//   TYPE-03
  "scripts": {
    "watch-sass": "sass --watch sass/main.scss css/style.css",
    "go-live": "set PORT=9000 && live-server --browser=chrome",
    "start": "npm-run-all --parallel go-live  watch-sass",
    "compile-sass": "node-sass sass/main.scss css/style.comp.css",
    "prefix-css": "postcss --use autoprefixer -b 'last 10 versions' css/style.comp.css -o css/style.prefix.css",
    "compress-css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build-css": "npm-run-all compile-sass prefix-css compress-css"
  },
```

`npm install autoprefixer concat live-server nodemon npm-run-all postcss-cli sass --save-dev`

```json
  "devDependencies": {
    "autoprefixer": "^10.4.13",
    "concat": "^1.0.3",
    "live-server": "^1.2.2",
    "node-sass": "^8.0.0",
    "nodemon": "^2.0.20",
    "npm-run-all": "^4.1.5",
    "postcss-cli": "^10.1.0",
    "sass": "^1.56.1"
  }

```
