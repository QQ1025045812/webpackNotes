# webpackNotes
## webpack入门
### 什么是 Webpack
**Webpack** 是一个模块打包器。它将根据模块的依赖关系进行静态分析，然后将这些模块按照指定的规则生成对应的静态资源。


![pic](http://a2.qpic.cn/psb?/V140svQu3Og1b3/vMAY0ftCgZawLAOgDNHr*3M5*QK6*Cj8HYTAVNvyDNE!/b/dGwBAAAAAAAA&bo=tQJBAbUCQQEDCSw!&rf=viewer_4)


### 为什么重复造轮子
  　　市面上已经存在的模块管理和打包工具并不适合大型的项目，尤其单页面 Web 应用程序。最紧迫的原因是如何在一个大规模的代码库中，维护各种模块资源的分割和存放，维护它们之间的依赖关系，并且无缝的将它们整合到一起生成适合浏览器端请求加载的静态资源。
    
    
这些已有的模块化工具并不能很好的完成如下的目标：

- 将依赖树拆分成按需加载的块
- 初始化加载的耗时尽量少
- 各种静态资源都可以视作模块
- 将第三方库整合成模块的能力
- 可以自定义打包逻辑的能力
- 适合大项目，无论是单页还是多页的 Web 应用


### Webpack的特点和优势
Webapck 和其他模块化工具有什么区别呢？
#### 代码拆分
Webpack 有两种组织模块依赖的方式，同步和异步。异步依赖作为分割点，形成一个新的快。在优化了依赖树后，每一个异步区块都作为一个文件被打包。
#### Loader
Webpack 本身只能处理原生的 JavaScript 模块，但是 loader 转换器可以将各种类型的资源转换成 JavaScript 模块。这样，任何资源都可以成为 Webpack 可以处理的模块。
#### 智能解析
Webpack 有一个智能解析器，几乎可以处理任何第三方库，无论它们的模块形式是 CommonJS、 AMD 还是普通的 JS 文件。甚至在加载依赖的时候，允许使用动态表达式 require("./templates/" + name + ".jade")。
#### 插件系统
Webpack 还有一个功能丰富的插件系统。大多数内容功能都是基于这个插件系统运行的，还可以开发和使用开源的 Webpack 插件，来满足各式各样的需求。
#### 快速运行
Webpack 使用异步 I/O 和多级缓存提高运行效率，这使得 Webpack 能够以令人难以置信的速度快速增量编译。


