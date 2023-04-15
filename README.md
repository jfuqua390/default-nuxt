# My customized Nuxt3 Minimal Starter

This repo is my starter for any future Nuxt3 projects. It has tailwind and pug installed by default.

## Setup

Make sure to install the dependencies:
```bash
# yarn
yarn install
```

## Manual Setup

```bash
#yarn
npx create-nuxt-app <project-name>
cd <project-name>
// Install tailwind
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
--follow a few steps on tailwindcss

yarn add pug
yarn add --dev prettier @prettier/plugin-pug

yarn add -D @tailwindcss/forms
yarn add -D @tailwindcss/container-queries
yarn add -D tailwind-scrollbar
--add these to tailwindconfig
require('@tailwindcss/forms'),
require('@tailwindcss/container-queries'),
require('tailwind-scrollbar')
```

## Development Server

Start the development server on `http://localhost:3000`

```bash
npm run dev
```

## Production

Build the application for production:

```bash
npm run build
```

Locally preview production build:

```bash
npm run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
