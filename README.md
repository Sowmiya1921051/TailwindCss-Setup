# Tailwind CSS v4 + PostCSS Setup (2025)

This guide outlines the complete and final process to set up **Tailwind CSS v4** with **PostCSS** and **Vite**.

---

## ✅ Step 0: Install Node.js

Make sure you have **Node.js (v18 or later)** installed.

---

## ✅ Step 1: Project Setup

```bash
mkdir my-tailwind-app
cd my-tailwind-app
npm init -y
```

##  ✅ Step 2: Install Required Packages

npm install -D tailwindcss@latest postcss@latest autoprefixer@latest vite


##  ✅ Step 3: Create Tailwind and PostCSS Config Files

npx tailwindcss init -p

### This creates:

tailwind.config.js

postcss.config.js

##  ✅ Step 4: Create Your CSS File

Create a style.css file in the root of your project and add:

@tailwind base;
@tailwind components;
@tailwind utilities;

##  ✅ Step 5: Configure tailwind.config.js

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}

##  ✅ Step 6: Configure postcss.config.js

module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}

##  ✅ Step 7: Configure package.json Scripts

Add this to your scripts:
"scripts": {
  "start": "vite"
}

##  ✅ Step 8: Create index.html File

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tailwind 4 with PostCSS</title>
  <link href="/style.css" rel="stylesheet">
</head>
<body>
  <h1 class="bg-red-500 text-white p-4">Hello Tailwind CSS v4!</h1>
</body>
</html>


##  ✅ Step 9: Run the Dev Server

npm run start
Visit: http://localhost:5173

##  ✅ Step 10: Install VS Code Extensions (Recommended)

Install the following extension:

Tailwind CSS IntelliSense

##  ✅ Optional: .gitignore File

node_modules/
dist/
.env
.vscode/
.DS_Store
