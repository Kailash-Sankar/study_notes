## Application Setup

- Overview
  - https://www.freecodecamp.org/news/how-to-set-up-deploy-your-react-app-from-scratch-using-webpack-and-babel-a669891033d4/
  - use eslint recommended react config and not the one suggessted above as it's no longer maintained.

- Webpack setup
  - https://webpack.js.org/guides/production/

- Optimizations
  - https://github.com/webpack-contrib/webpack-bundle-analyzer
  - https://webpack.js.org/plugins/mini-css-extract-plugin/#minimizing-for-production
  - http://chrisbateman.github.io/webpack-visualizer/

- Testing
  - https://www.freecodecamp.org/news/how-to-set-up-jest-enzyme-like-a-boss-8455a2bc6d56/

- File structure
  - https://medium.com/@Charles_Stover/optimal-file-structure-for-react-applications-f3e35ad0a145

- Hooks
  - https://medium.com/netscape/git-hooks-with-husky-8b98f2556363

- CSS Modules setup
  - https://stackoverflow.com/a/58190532/1878459

- Polyfills
  - Use core.js to add polyfills for different targets. Enable debug in babel to verify. 
  - jest env (jsdom) won't match the label browsers, keep a lower targer or override to have polyfills
  - https://babeljs.io/docs/en/babel-preset-env
