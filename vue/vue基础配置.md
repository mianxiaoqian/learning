<!--
 * @Author: qianqian.zhao
 * @Date: 2020-04-02 15:53:38
 * @LastEditors: qianqian.zhao
 * @LastEditTime: 2020-04-03 14:44:07
 * @Description: 
 -->
vue一些引入版本：
runtime-only就是运行时版本，不包含编译器
而编译器的作用就是将模板字符串编译为js渲染函数的代码

vue-loader 15版本以上的使用必须搭配vue-loader-plugin使用
webpack.config.js引用vue-loader-lugin时，需要从vue-loader/lib/plugin引用vue-loader-plugin

vue页面渲染空白，而且控制台无报错信息
在vue源码内打断点，发现在渲染之前绑定的节点是正确的，页面也已经出现占位。
结果执行完渲染函数，页面就空白了。
是不是什么错误信息未暴露出来啊，哭唧唧33  


1、Vue.prototype 下的属性和方法的挂载主要是在 src/core/instance 目录中的代码处理的

2、Vue 下的静态属性和方法的挂载主要是在 src/core/global-api 目录下的代码处理的

3、web-runtime.js 主要是添加web平台特有的配置、组件和指令，web-runtime-with-compiler.js 给Vue的 $mount 方法添加 compiler 编译器，支持 template。