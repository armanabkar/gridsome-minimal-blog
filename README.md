# Gridsome Minimal Blog

A blog starter theme for [Gridsome]() with a minimalistic design.

### [Live Demo](https://armanabkar.github.io/gridsome-minimal-blog/)

## Installation

### 1. Install Gridsome CLI tool if you don't have

`npm install --global @gridsome/cli`

### 2. Create a Gridsome project

1. `gridsome create my-blog https://github.com/armanabkar/gridsome-minimal-blog` to install default starter
2. `cd my-blog` to open the folder
3. `gridsome develop` to start a local dev server at `http://localhost:8080`
4. Happy coding 🎉🙌

## Build (& Deploy)

1. `npm run build` to build the project and output it to /dist folder.
2. optional: `npm run deploy` to deploy it to GitHub Pages, you should also configure gridsome.config.js file:

```js
{
  siteUrl: "https://armanabkar.github.io",
  pathPrefix: "/gridsome-minimal-blog",
}
```