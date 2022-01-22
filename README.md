# fresh-project

simple project setup command

Laravel mix documentaion
````
https://laravel-mix.com/docs/5.0/installation
````

````
npm init -y
npm install laravel-mix --save-dev
````

create webpack file
````
const mix = require('laravel-mix');

mix.js('src/js/app.js', 'public/js')
.sass('src/scss/app.scss', 'public/css')

````

update/add this  script in packege.json file

````
"scripts": {
"dev": "npm run development",
"development": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
"watch": "npm run development -- --watch",
"hot": "cross-env NODE_ENV=development node_modules/webpack-dev-server/bin/webpack-dev-server.js --inline --hot --config=node_modules/laravel-mix/setup/webpack.config.js",
"prod": "npm run production",
"production": "cross-env NODE_ENV=production node_modules/webpack/bin/webpack.js --no-progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js"
}
````


add cross env

````
npm install cross-env --save-dev
````