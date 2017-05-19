# webpackNotes
## webpack入门
### 什么是 Webpack
**Webpack** 是一个模块打包器。它将根据模块的依赖关系进行静态分析，然后将这些模块按照指定的规则生成对应的静态资源。
![pic](http://a2.qpic.cn/psb?/V140svQu3Og1b3/vMAY0ftCgZawLAOgDNHr*3M5*QK6*Cj8HYTAVNvyDNE!/b/dGwBAAAAAAAA&bo=tQJBAbUCQQEDCSw!&rf=viewer_4)
### 为什么重复造轮子
  　　市面上已经存在的模块管理和打包工具并不适合大型的项目，尤其单页面 Web 应用程序。最紧迫的原因是如何在一个大规模的代码库中，维护各种模块资源的分割和存放，维护它们之间的依赖关系，并且无缝的将它们整合到一起生成适合浏览器端请求加载的静态资源。
    
    
这些已有的模块化工具并不能很好的完成如下的目标：

－　将依赖树拆分成按需加载的块
－　初始化加载的耗时尽量少　

