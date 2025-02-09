# GE-Job-Sim
I have built Vue.js UI for GE Aerospace Digital Frontend development team as part of curriculum on Forage platform. The language I was instructed to use is JavaScript, Vue 3 framework 🚀

## Key Features: 

1. Declarative Rendering:
Use HTML templates with Vue's special directives like v-for, v-if, and v-bind to bind data dynamically.
```bash
<form class="submit class" v-if="!editing">
</form>
```

2. Component-Based Architecture:
Build reusable, self-contained components that manage their state and behavior. 

3. Reactivity System:
Automatically updates the DOM when the underlying data changes, providing a seamless UI experience. 

4. Directives:
Built-in commands like v-model (two-way binding), v-on (event listeners), and v-bind (dynamic attributes).
```bash
<input v-model="productA/A1" type="number" placeholder="type number">
</input>
```
5. Computed Properties:
   ```bash
   import { ref, computed } from 'vue'
   ```
I used Vite to create a Vue.js project 👋

Here is the typical folder structure for a Vue project created with Vite:
```bash
app/
├── node_modules/
├── public/
│   └── vite.svg
├── src/
│   ├── assets/
│   ├── components/
│   ├── views/
│   ├── App.vue
│   ├── main.js
│   └── index.css
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
├── vite.config.js
└── README.md
```
# Folder and File Overview 

1. node_modules/ 

Contains all npm dependencies and packages required by the project. You generally don’t interact directly with this folder.

2. public/ 

Files in the public folder are served as static assets and are accessible directly in the browser. 

3. src/ 

This is the main working directory where application code resides. 

- assets/ 

Contains static assets like images, fonts, or stylesheets. 

Files in this folder can be imported directly into components or JavaScript files. 

- components/ 

Stores reusable Vue components that encapsulate smaller parts of the UI. 

- App.vue 

The root component of my application, where all other components are nested.
html:
```bash
<template>
  <div id="app">
    <router-view />
  </div>
</template>
```
- main.js 

The entry point of application where the Vue app is initialized and mounted. 

Script:
```bash
import { createApp, computed } from 'vue';
import App from './App.vue';
import './index.css'; 

createApp(App).mount('#app');
```
- index.css

A global CSS file that applies styles to app. You can rename or replace it with SCSS or other preprocessors.

4. index.html

This is the main HTML template for the application. It includes the root element where the Vue app is mounted. Vite processes this file during development and builds.
html:
```bash
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vite + Vue</title>
  </head>
  <body>
    <div id="app"></div>
    <script type="module" src="/src/main.js"></script>
  </body>
</html>
```
5. vite.config.js 

This is the configuration file for Vite. It allows customization of the development server, build process, plugins, and more. 

Config:
```bash
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue' 

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [vue()],
})
```
6. .gitignore

Specifies files and folders that Git should ignore.

7. package.json

Defines project dependencies, scripts, and metadata.

Json:
```bash
{
  "name": "vite-vue-starter",
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "serve": "vite preview"
  },
  "dependencies": {
    "vue": "^3.5.13"
  },
  "devDependencies": {
    "@vitejs/plugin-vue": "^5.2.1",
    "vite": "^6.0.7"
  }
}
```
