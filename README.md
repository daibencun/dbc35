
# Webpack

## `nrm`的安装使用

- 作用：提供了一些最常用的NPM包镜像地址，能够让我们快速的切换安装包时候的服务器地址；

- 什么是镜像：原来包刚一开始是只存在于国外的NPM服务器，但是由于网络原因，经常访问不到，这时候，我们可以在国内，创建一个和官网完全一样的NPM服务器，只不过，数据都是从人家那里拿过来的，除此之外，使用方式完全一样；

1、运行`npm i nrm -g`全局安装`nrm`包；
2、使用`nrm ls`查看当前所有可用的镜像源地址以及当前使用的镜像源地址
3、使用`nrm use npm`或`nrm use taobao`切换不同的镜像源地址

>注意：nrm 只是单纯的提供了几个常用的 下载包的 URL 地址，并能够让我们在 这几个 地址之间，很方便的进行切换，但是， 我们每次装包的时候，使用的装包工具， 都是 npm

## 在网页中会引用哪些常见的静态资源

- JS
  - .js .jsx .coffee .ts(TypeScript 类C# 语言)
- css
  - .css .less .sass .scss
- Images
  - .jpg .png .gif .bmp .svg
- 字体文件（Fonts）
  - .svg .ttf .eot .woff .woff2
- 模板文件
  - .ejs .jade .vue(这是在webpack 中定义组件的方式，推荐这么用)

## 网页中引入的静态资源多了以后有什么问题

- 网页加载速度慢，因为 我们要发起很多的二次请求；
- 要处理错综复杂的依赖关系

## 如何解决上述两个问题

- 合并、压缩、精灵图、图片的Base64编码
- 可以使用之前学过的 requiresJS、也可以使用webpack可以解决各个包之间的复杂依赖关系；

## 什么是webpack

- webpack 是前端的一个项目构建工具，它是基于 Node.js  开发出来的一个前端工具

## 如何完美解决上述两种解决方案

- 使用Gulp, 是基于 task 任务的；
  - 小巧、方便、灵活、任务的灵活处理
- 使用 Webpack ，是基于整个项目进行构建的；
- 借助于webpack 这个前端自动化构建工具，可以完美实现资源的合并、打包、压缩、混淆、处理依赖关系等诸多功能；
- 根据官网的图片介绍webpack 打包的过程
  - [webpack官网]`（http://webpack.github.io/）`

## webpack安装的两种方式

1、运行`npm i webpack -g`全局安装webpack,这样就能在全局使用webpack的命令
2、在项目根目录中运行`npm i webpack --save-dev`安装到项目依赖中

## 初步使用`webpack`打包构建列表隔行变色案例

1.运行`npm init`初始化项目，使用npm管理项目中的依赖包
2.创建基本项目的目录结构
3.使用`cnpm i jquery -save`安装juery类库
4.创建`main.js`并书写隔行变色的逻辑代码
```
  <!-- 导入jquery类库 -->
  import $ from 'jquery'
  <!-- 设置偶数行背景色，索引从0开始，0是偶数 -->
  $('#list li:even').css('backgroundColor','lightblue');
  <!-- 设置奇数行背景色 -->
  $('#list li:odd').css('backgroundColor','pink');

```
