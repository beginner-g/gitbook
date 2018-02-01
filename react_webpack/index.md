# React-webpack全栈开发项目

## 工程架构

 - webpack配置
 - node服务
 - 服务端渲染

## web 开发常用网络优化

 - 合并资源文件，减少HTTP请求
 - 压缩资源文件减小请求大小
 - 利用缓存机制，减少请求

## 构建Webpack配置

模块打包器
loader处理工具
- npm init 配置npm项目（生成package.json文件里面所依赖的包）
- npm i webpack
- npm i react
- 创建build文件夹（放webpack的config配置文件及脚本文件）
- 创建client文件夹（放前端文件）

在build文件夹下创建webpack.config.js文件，代码如下：

~~~js
const path = require('path')
module exports = {
  entry: {
    app: path.join(_dirname,'../client/app.js')
  },
  output: {
    filename: '[name].[hash].js',
    path: path.join(_dirname,'../dist'),
    publishPath: '/public'
  }
}
~~~

 - 在package.json文件的scripts里添加(“build”:"webpack --config build/webpack.config.js")
 - 命令行输入 npm run build


## Webpack loader 应用

- npm i react-dom 把react渲染在dom里

- 配置webpack loader

  npm i babel-loader -D
  npm i babel-core -D
  npm run build 

~~~js
const path = require('path')
module exports = {
  ...
  module: {
    rules: [
      {
        test: /.jsx$/,
        loader: 'babel-loader'
      }
    ]
  }
}
~~~
