从零创建 webapck react 工程

1、首先使用 npm init 创建一个前端项目
```js
mkdir my-app
cd my-app
npm init -y
```
2、安装 webpack
```javascript
npm i -D webpack webpack-cli webpack-dev-server html-webpack-plugin
```
webpack - 前端构建工具
webpack-cli - 让 webpack 支持命令行执行
webpack-dev-server - 开发模式下启动服务器，修改代码，浏览器会自动刷新。


3、 安装 babel
babel： 可以将 es6 代码转变为 es5，
@babel/preset-react： 让 babel 支持 react 的预设
babel-loader：是让 webpack 支持 babel 的加载器

```javascript
npm i -D @babel/core @babel/preset-env @babel/preset-react babel-loader
```
在项目更目录新建一个 babel.config.js 文件，将安装的 babel 写入这个文件，babel 会在运行前读取这份配置文件
```javascript
module.exports = {
  presets: ['@babel/preset-env', '@babel/preset-react'],
}

```

安装 CSS 加载器
```js
npm i -D style-loader css-loader
```
css-loader 用于解析 css 文件； style-loader 会通过使用多个 <style></style>标签的形式自动把 styles 插入到 DOM 中。

安装 react 和 react-dom
```js
npm i react react-dom
```

建一个 index.html 文件
 创建一个在public目录，并且在下面新建一个index.html 文件。

 新建一个  `index.js `文件
创建一个名为 src 的文件夹，所有源代码都放在该目录下，在src目录下，创建index.js文件，该文件也就是 webpack 构建的入口文件
创建文件
 `src/index.js` webpack 构建的入口文件
 `src/App.js`  组件
 在项目根目录创建一个 `webpack.config.js` 文件， `webpack.config.js` 是 webpack 的默认配置文件名