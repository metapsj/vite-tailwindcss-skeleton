# setup

---

npm init @vitejs/app

npm install tailwindcss@latest postcss@latest autoprefixer@latest --save-dev

npx tailwindcss init -p

---

# style.css

remove generated css

@tailwind base;
@tailwind components;
@tailwind utilities;

---

# main.js

remove vite generated code

---

# index.html

<link rel="stylesheet" href="/style.css">

<!-- inside div.app -->
<h1 class="text-3xl md:text-5xl text-gray-500 text-center font-semibold mx-auto">
  Hello, is this working?
</h1>

---

# plugins

npm install @tailwindcss/forms @tailwindcss/aspect-ratio --save-dev

---

# tailwind.config.js

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

---

# alpine.js to index.html or main.js

<script src="alpine.min.js" defer></script>

---

# purgecss to tailwind.config.js

purge: [
"./index.html"
]

---