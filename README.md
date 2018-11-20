# evitt-website
Landing page for Evitt

## Building the project
When making changes to any SCSS files, you will need to rebuild the project:
```bash
npm run css
```

## Running locally
- Install nvm (Node Version Manager) using the directions at https://github.com/creationix/nvm#installation
- `nvm use`
- `npm install`
- `npm start`
- Run a local server in the `public/` directory

Whenever you enter this repo's directory, you should always run `nvm use` before doing anything, so that you use our sanctioned version of Node.

## Deploying to Github Pages
We use the `gh-pages` npm module to manage deployment to Github Pages

First pre-compile and minify CSS:
```bash
npm run css
```

**Note:** Make sure `public/index.html` is referencing the minified CSS file

Then deploy to Github Pages:
```bash
npm run deploy
```

This will publish only the contents of the `public/` folder to the `gh-pages` branch