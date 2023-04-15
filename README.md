# My customized Nuxt3 Minimal Starter

This repo is my starter for any future Nuxt3 projects. It has tailwind and pug installed by default.

## Quick Setup

To do a quick setup, download zip and run yarn install

```bash
# yarn
yarn install
```

## Manual Setup

Just how I set it up in case I need this in the future

```bash
#Initialize Nuxt
npx create-nuxt-app <project-name>
cd <project-name>
yarn install

#Install tailwind
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init

#Add this to nuxt.config.ts
postcss: {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
    ...(process.env.NODE_ENV === 'production' ? { cssnano: {} } : {})
  },
},

#Add this to tailwind.config.js
content: [
  "./components/**/*.{js,vue,ts}",
  "./layouts/**/*.vue",
  "./pages/**/*.vue",
  "./plugins/**/*.{js,ts}",
  "./nuxt.config.{js,ts}",
  "./app.vue",
],

#Create a ./assets/css/main.css and add this
@tailwind base;
@tailwind components;
@tailwind utilities;

#Add this to tailwind.config.ts
css: ["~/assets/css/main.css"],

#Tailwind plugins I like
yarn add -D @tailwindcss/forms
yarn add -D @tailwindcss/container-queries
yarn add -D tailwind-scrollbar

#Add these to tailwind.config.js - under plugins
plugins: [
  require('@tailwindcss/forms'),
  require('@tailwindcss/container-queries'),
  require('tailwind-scrollbar')
],

#pug
yarn add pug
yarn add --dev prettier @prettier/plugin-pug

#Add separator to tailwind.config because of pug conflicts
separator: "_",

```

## Development Server

Start the development server on `http://localhost:3000`

```bash
yarn dev -o
```

## Devtools

Using Nuxt dev tools - https://devtools.nuxtjs.org/guide

## Production

Build the application for production:

```bash
yarn build
```

Locally preview production build:

```bash
yarn preview
```

## Packages

Tailwind -
Pug -
