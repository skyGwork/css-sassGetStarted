## Contents

- Config - font - contents - button, a, forms, autoWidth

> GoogleFonts

- To embed a font, copy the code into the <head> of your html

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Comfortaa:wght@400;500&family=Lato&family=Noto+Sans:wght@400;600&family=Poppins:wght@400;500;600;700&family=Yeseva+One&display=swap"
  rel="stylesheet"
/>
```

- @import

```css
@import url('https://fonts.googleapis.com/css2?family=Comfortaa:wght@400;500&family=Lato&family=Montserrat:wght@400;500;600;700;800;900&family=Noto+Sans:wght@400;600&family=Poppins:wght@400;500;600;700&family=Yeseva+One&display=swap');
```

- CSS rules to specify families

```css
font-family: 'Comfortaa', cursive;
font-family: 'Lato', sans-serif;
font-family: 'Montserrat', sans-serif;
font-family: 'Noto Sans', sans-serif;
font-family: 'Poppins', sans-serif;
font-family: 'Yeseva One', cursive;
```

```bash
$touch _mixin.scss _mediaQ.scss _reSet.scss _util.scss _var.scss
$npm install autoprefixer concat nodemon npm-run-all postcss-cli sass --save-dev
```

> Main.scss

```scss
@import 'config/var';
@import 'config/mediaQ';
@import 'config/reSet';
@import 'config/util';
@import 'config/mixin';
@import 'app/app';
@import 'app/views/home';
@import 'app/components/header';
```

> NPM

- ? todo npm-run-all

```bash
$npm install package-name
$npm i package-name

$npm uninstall package-name
$npm un package-name

$npm install autoprefixer concat nodemon npm-run-all postcss-cli sass --save-dev
$npm i live-server --save-dev

$npm uninstall -D package-name
$npm uninstall --save-dev package-name

$npm run compile-sassile-sass
$npm run go-live
```
