##使用LESS优化极客学院页面CSS
本次作业主要使用less优化之前的极客学院作业。

###less部分
之前的极客学院是使用seajs模块化，同时将css，js，html都进行了模块化。因此之前的极客学院作业的CSS是分布在多个css文件中。  
本次作业将所有的css重写为LESS到一个文件中。主要的思路是分为三个less文件
1. base.less        主要是涉及到一些公共的模块和工具，和颜色定义。不生成单独的css。
2. scalffold.less   主要是定义了主体框架结构。只有布局，不含样式。
3. module.less      将页面中的内容都定义成了模块。含有模块本身的布局。
4. style.less       编译入口文件，用于统一引入所有需要的less文件。

###gulp部分
本次作业并没有使用到复杂的gulp流程，只是设计了两个简单的流程
1. dev  用于开发环境使用，主要是观察less文件，当有less文件变化，则编译style.less文件并输出style.css
2. release 用于发布，一次性任务，将所需要的less编译成style.css文件。


###感想，和问题
用了LESS，发现已经完全回不去了。但是没有if判断，所以感觉在某些方面还是有些束缚。
另外比较痛苦的是CSS的结构化和面向对象的思路不是很清晰。不知道老师是否有好的思路。  
之前有用过bootstrap，但是这个bootstrap感觉还是不能用于平时的页面开发。主要是样式过于统一了，定制化还不如重写。脚手架值的参考。但是古估计在像素眼的美工面前还是不能用。
所以，感觉平时做页面，要是把css分的特别细碎，使用起来感觉太凌乱，如果集成起来成组件，感觉又容易陷入传统的思路中去，导致单个组件太庞大，组件重用度不高。
本次作业，耗费了较多时间在考虑less分层，面向对象的思路中。所以对于gulp的部分并未做过多的工作。考虑到上周的fis学习中也看了很多gulp的内容。所以这周gulp并为设计整个项目的工作流。