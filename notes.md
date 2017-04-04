# Have Completed
* create project
* yarn init
* git init
* create webpack.config.js
* yarn add webpack --dev
* .gitignore
  * add yarn.lock at the bottom of .gitignore
* npm install sass
* fill webpack.config.js with the following:
* (add README.md if desired, or add later)

```
var path = require('path');

module.exports = {
  entry: ['./app/index.js', './app/styles/main.sass'],
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist')
  },
  devtool: "cheap-eval-source-map",
  watch: true,
  module: {
        rules: [{
            test: /\.sass$/,
            use: [{
                loader: "style-loader" // creates style nodes from JS strings
            }, {
                loader: "css-loader" // translates CSS into CommonJS
            }, {
                loader: "sass-loader" // compiles Sass to CSS
            }]
        }]
    }
};
```
* install:
  * ```npm install sass-loader --save-dev```
  * ```npm install css-loader --save-dev```
  * ```npm install style-loader --save-dev```
* include script tag in html:
```<script type="text/javascript" src="./dist/bundle.js"></script>```
* create GitHub repo
* set up remote
* commit
* push
