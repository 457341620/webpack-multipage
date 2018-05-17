# react app 多页面配置

## 目的
- 增加多页面配置(不只是react)
- 配置html里面写代码
- 增加html可以require HTML页面作为模块渲染html
- 增加html里面可以通过require图片打包

## 功能
- 支持直接在public里面写html(不过需要每次添加html,都要修改配置文件)
- 支持在html里面直接require html页面
```
  <!-- public/index.html -->
    <%= require('html-loader!./partials/header.html')  %>  
```
- 支持html里面require图片(正常情况下不用require(图片路径)是不会打包的)
```
  <!-- public/index.html -->
  <img src="<%= require('../src/imgs/phone.png')  %>" >
```

## 参考
- <a href="https://segmentfault.com/a/1190000012772616" target="_blank">参考博客</a>
- <a href="https://github.com/facebook/create-react-app" target="_blank">create-react-app</a>

## sass配置是参考create-react-app 里面的 所以引用的时候需要找到css目录

## 此模板下如何添加一个页面
+ 在public下添加html
+ 终止运行
+ ``` yarn start ```

## feture
- [ ]通过命令增加html页面，无须改配置