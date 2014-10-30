Move-To-Mobile-Web
==================

Mobile Web Development Wiki &amp; Guide 

Guide List
===========

- Traditional FE > Mobile FE 
  - 上层建筑
    - [html: meta](https://github.com/hongru/Move-To-Mobile-Web/wiki/html:meta-&-html:link) 
    - [css:绝对流体布局 border-box & 百分比的运用](https://github.com/hongru/Move-To-Mobile-Web/wiki/css:%E8%87%AA%E9%80%82%E5%BA%94%E5%B8%83%E5%B1%80-&-border-box%E7%9A%84%E5%BA%94%E7%94%A8)
    - [css:background-size & padding 的运用](https://github.com/hongru/Move-To-Mobile-Web/wiki/css:background-size-&-padding-%E7%9A%84%E4%BD%BF%E7%94%A8)
    - [css:@media queries](https://github.com/hongru/Move-To-Mobile-Web/wiki/Media-Queries)
    - [css: transition|animation|touch scrolling](https://github.com/hongru/Move-To-Mobile-Web/wiki/css:transition%7Canimation%7Coverflow-scrolling)
    - [css: ratina 适配](https://github.com/hongru/Move-To-Mobile-Web/wiki/Retina%E7%9A%84%E9%80%82%E9%85%8D)
    - [js:mobile features [touch events, history, deviceRatio, deviceoritation, localstorage, devicemotion, standalone]](https://github.com/hongru/Move-To-Mobile-Web/wiki/%E3%80%90mobile-web%E3%80%91js-features)
  - 底层基础
    - webapp:OPOA的架构和思路[backbone, kissy-mobile]
    - webapp:模版前端化
    - webapp:mvc|mvp的文件组织和规范
    - 资源适配image|css:从前端出发的解决方案
    - 资源适配image|css:从后端出发的解决方案

- Mobile Web Performance|Experience
  - http 握手
  - click vs touchstart
  - overflow-scrolling
  - transition vs style
  - Gesture:原理和应用
  - 新奇特的bugs:见Araw dev wiki

- Mobile Web Test & Debug
  - chrome的运用
  - Macbook Safari + iphone
  - Xcode Simulator
  - 网络代理，抓请求，配host

- More【下次...】
  - Mobile Web & Native的融合...
    - 跳转协议和规范
    - js bridge
    - js-binding

------------------------

Mobile Performance
====

## 发现问题

- 工具使用
  - Charles
  - 摩天轮MTL
  - MF
- 从数据开始，以数据结束
  - 获得真实用户端瀑布图
  - 关键节点的打点和监控

## 分析问题

- 性能问题分类
  - 加载性能问题
  - 渲染性能问题
  - 交互性能问题
- 性能问题定位

## 解决问题

- 加载性能问题解决条例
  * 首次图片请求是否过多
  * 单张图片或者图片的平均size是否过大
  * css脚本资源是否拆分太细，css链接数过多
  * css是否有过多冗余
  * js脚本是否合理Combo（单个文件过大或者js脚本连接数过多）
  * cdn或者mt的配置数据请求数是否合理
  * mtop请求数是否合理
  * manifest是否合理使用
  * iconFont是否合理使用
  * 所有图片是否域名收敛
  * 所有css和js脚本是否域名收敛
  * 是否有使用服务端302跳转的图片，比如根据userid拼头像
  * 异步数据的串并行是否合理
- 渲染问题解决条例
- 交互性能解决条例
