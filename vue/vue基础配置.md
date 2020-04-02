<!--
 * @Author: qianqian.zhao
 * @Date: 2020-04-02 15:53:38
 * @LastEditors: qianqian.zhao
 * @LastEditTime: 2020-04-02 17:19:49
 * @Description: 
 -->
vue一些引入版本：
runtime-only就是运行时版本，不包含编译器
而编译器的作用就是将模板字符串编译为js渲染函数的代码

vue-loader 15版本以上的使用必须搭配vue-loader-plugin使用
webpack.config.js引用vue-loader-lugin时，需要从vue-loader/lib/plugin引用vue-loader-plugin