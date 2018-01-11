# 基础知识

它是一个前端资源加载、打包工具，将 **根据模块的依赖关系** 进行静态分析，并 **依据规则** 生成对应的静态资源

# 框架安装

全局安装 `npm` \ `NodeJS` \ `webpack`

# 打包使用

## 1.简单的打包
单个文件的打包
使用命令：`webpack 需要打包的文件名 打包后的文件名`

导出模块：`module.exports = 导出的内容;`
写入模块：`require('写入的文件路径');`

同一个文件下，路径前加上 '`./`'

## 2.样式的打包

通过安装 `loader` 加载器，可以将静态的样式文件，一同打包到 `bundle.js` 文件中，通过下列命令安装加载器：
```
npm install css-loader style-loader
```
`css-loader` 的作用是，遍历样式文件里面的代码，如果发现有 `@import` 样式引入，就会执行引入

`style-loader` 的作用是，将我们的样式，直接通过 `style` 标签插入到页面的头部
```
// 表示是一个特殊的文件 '!style-loader!css-loader!' 是固定的写法
require('!style-loader!css-loader!./style.css');
document.write(js1('<div>sdf</div>'));
```



