# evitt-website
Landing page for Evitt

## Building the project
When making changes to any SCSS files, you will need to rebuild the project:
```bash
npm run css:dev
```

Alternatively, you can watch for changes while developing:
```bash
npm run watch:css
```

**Note:** This will only compile and autoprefix the CSS, not minify it. This is mainly done for speed during development

## Running locally
- Install nvm (Node Version Manager) using the directions at https://github.com/creationix/nvm#installation
- `nvm use`
- `npm install`
- `npm watch:css`
- Run a local server in the `public/` directory

Whenever you enter this repo's directory, you should always run `nvm use` before doing anything, so that you use our sanctioned version of Node.

## Deploying to Github Pages
We use the `gh-pages` npm module to manage deployment to Github Pages


1. First make sure `public/index.html` is referencing the minified CSS file
2. `npm run css:prod`
3. Add and commit your local changes (make sure you also commit the minified CSS file)
4. `npm run deploy`

This will prepare all SCSS for production and publish only the contents of the `public/` folder to the `gh-pages` branch

**NOTE:** Don't delete the CNAME file. WIthout it the custom domain on Github Pages breaks. ANy time the domain needs to be changed, it should be changed manually in the CNAME file