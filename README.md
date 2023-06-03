# storybook-tailwind-dark-theme-toggle

## Installation

Install the following npm module:

```sh
npm i --save-dev storybook-tailwind-dark-theme-toggle
```

or with yarn:

```sh
yarn add -D storybook-tailwind-dark-theme-toggle
```

Then, add following content to `.storybook/main.js`

```js
module.exports = {
  addons: ['storybook-tailwind-dark-theme-toggle'],
};
```

### Make sure tailwind is configured to use the darkmode class in the `tailwind.config.js`

```js
module.exports = {
  darkMode: 'class',
  // ...
} 
```


### Set Dark Mode as default

To set dark mode as default, Add the following lines of code to your preview.js file

```js
const preview = {
  globalTypes: {
    darkMode: {
      defaultValue: true, // Enable dark mode by default on all stories
    },
    // Optional (Default: 'dark')
    className: {
      defaultValue: 'custom-classname', // Set your custom dark mode class name
    },
    // Optional
    selector: {
        defaultValue: "html"
    }
  },
};
```
