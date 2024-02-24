# React + TypeScript + Vite

This template provides a boilerplate setup to get React working in Vite with HMR, Eslint, Prettier, Vitest and the Image-tool plugin of Vite.


_Note: The initial project was created with_

```js
npm create vite@latest . -- --template react-swc-ts
```

## Extra tools added

### Tailwind

- https://github.com/tailwindlabs/prettier-plugin-tailwindcss

- https://tailwindcss.com/docs/guides/vite

```js
npm install -D tailwindcss clsx autoprefixer postcss

npx tailwindcss init
```

and then configure tailwind.config.js along with postcss.config.js

### Prettier

```js
npm install -D prettier-plugin-tailwindcss @trivago/prettier-plugin-sort-imports prettier eslint-config-prettier
```

Configure .prettierc & .prettierignore files

### Image tool vite plugin

```js
npm install -D vite-imagetools
```

- Directives https://github.com/JonasKruckenberg/imagetools/blob/main/docs/directives.md#directives

### Set aliases in the vite.config and tsconfig files

tsconfig
```js
"paths": {
  "@/*": ["./src/*"],
},
```

vite.config
```js
resolve: {
  alias: {
    '@': path.resolve(__dirname, './src'),
  },
},
```

### Install vitest

```js
npm install vitest jsdom @testing-library/jest-dom @testing-library/react @types/node --save-dev
```

Add test script in package.json

```js
...
"test": "vitest"
...
```