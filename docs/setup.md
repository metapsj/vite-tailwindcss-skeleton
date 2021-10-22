# setup

## initialize project

```bash
npm init @vitejs/app
```

## install libraries

```bash
npm install tailwindcss@latest postcss@latest autoprefixer@latest --save-dev

```

## initialize tailwindcss

```bash
npx tailwindcss init -p
```

## style.css

remove generated css

add tailwind imports

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## main.js

remove vite generated code

## index.html

```html
<link rel="stylesheet" href="/style.css" />

<!-- insert into div.app -->
<h1
  class="text-3xl md:text-5xl text-gray-500 text-center font-semibold mx-auto"
>
  Hello, is this working?
</h1>
```

## install plugins

```bash
npm install @tailwindcss/forms @tailwindcss/aspect-ratio --save-dev
```

## configure plugins in tailwind.config.js

```javascript
const colors = require('tailwindcss/colors')

extend: {
  colors: {
    teal: colors.teal,
    cyan: colors.cyan,
  }
}

plugins: [
  require('@tailwindcss/forms'),
  require('@tailwindcss/aspect-ratio'),
]
```

## install alpinejs

```bash
npm install alpinejs --save-dev
```

## configure alpine.js in main.js

```javascript
import Alpine from "alpinejs";
window.Alpine = Alpine;
Alpine.start();
```

## configure purgecss in tailwind.config.js

```javascript
purge: ["./index.html"];
```
