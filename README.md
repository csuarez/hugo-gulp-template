# hugo-gulp-template
## What is this?
This is a template for **[Hugo](https://gohugo.io/)** projects. Hugo includes a CLI that serves to build projects, but it is a little bit limited when you want to compile and process your assets. This template enhances the standard Hugo workflow adding the following features:
* Compilation of **SCSS** source code.
* **Minification** for scripts, stylesheets and HTML code.
* **Uglification** for scripts.
* Addition of hashes to assets for **cache-busting**.
* **Optimization of images**.
* **Server** with **[LiveReload](http://livereload.com/)** support.
* Better **management of the configuration**, with separated environments.

## How to install it?
First of all, you need to have installed `hugo`, `npm` and `gulp`. In order to use it, you have to install its dependencies, by executing the following command in the template root folder:
```sh
$ npm install
```
And that's all!

## About the folder structure
This template adds two additional folders to an Hugo project:
* `/stylesheets`: Where you have to put your SCSS files. After the web building, the compiled files will be in `/public/css`.

* `/scripts`: Where you have to put your Javascript files. After the web building, the compiled files will be in `/public/js`.

## How to build the web
In the root folder you have to execute:
```sh
$ gulp build
```
This will generate the web, compile the SCSS code, minify all the code, optimize the images, uglify the Javascript and prepare the names of the assets for cache-busting and replace them in the HTML code. The result will be in the `/public` folder as a normal Hugo project.


## How to run the server
In the root folder you have to execute:
```sh
$ gulp serve
```
This will run a server in the **6789** port, with **LiveReload support**. Every time when the web or the assets change, the web will be rebuilt and reloaded in your browser.

## How to configure the project
By default, Hugo only uses one configuration file (`config.toml`) to define parameters like the base URL. When you are working in a real project, this parameters will be different between your development and your production environment. In order to manage this, this templates introduces two different configuration file: `config.dev.toml` and `config.prod.toml`.

This templates provides two commandos to swap between the production and the development configurations. To change to the development configuration:
```sh
$ gulp config-dev
```
To change to the production configuration:
```sh
$ gulp config-prod
```

By default, the server will use the development file always. It is **strongly recommended** to execute `config-prod` before the generation of a web which will be deployed in a production environment.

## LICENSE
Copyright (c) 2016 César Suárez Ortega

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
