<!--
 * @Author: qianqian.zhao
 * @Date: 2020-05-26 16:55:38
 * @LastEditors: qianqian.zhao
 * @LastEditTime: 2020-06-02 16:46:15
 * @Description: vue知识点
 -->

#### MVVM模型
model指的是数据，view指的是视图；
vm是一个桥梁，可以实现数据和视图的双向绑定；

#### vue的双向数据绑定
vue2.0是使用Object.definePrototype进行数据劫持，
然后收集每一个组件内的watch内的监听订阅
当数据发生变化时进行通知，使用了发布、订阅模式

vue3.0是是使用proxy进行的数据劫持；

Objetc.definePrototype与pxory的比较
1、 definePrototype需要对对象的每一个属性都进行处理，proxy可以直接监听一个大对象
2、 

vue对数组的监听

#### vue自定义组件上实现v-model

#### vue中nextTick的实现原理
主要是使用的事件循环。会分别判断promise、setImmediate、setTimeout、是否支持使用

#### vue的生命周期
beforeCreate 实例创建之前，什么都不存在
created 完成实例的创建，vm对象生成,data、prop、method、computed、watch等都已经可以使用
beforeMounte 挂载之前，先进行了占位；虚拟Dom创建完成
mounted 完成挂载，生成真实DOM节点
beforeUpdate
updated
beforeDestroy 实例销毁之前，数据都可以访问
destroyed 实例销毁，数据不可访问
关于keep-alive的生命周期
activated 使用keep-alive时，再次进入组件（组件被激活）会执行
deActivated 使用keep-alive时，组件被销毁时调用

#### vue的data为什么使用函数

#### vue虚拟DOM

#### vue生命周期在父子组件间的调用顺序

#### vue的通信方式
prop 父传子(是响应式的),$emit 子向父传递事件，$on 父组件接收，也可以在prop属性上增加async修饰符，进行事件接收的省略
不相关组件间（一般是组件跨级传递消息）使用EventBus发布订阅的on与emit
祖辈组件上下之间使用依赖注入provide与inject传递，提供的property是非响应式的
$attrs/$listeners ？ vue2.6新增
父可以使用ref调用子（ref只在组件渲染结束后生效，且不是响应式的），子可以使用$parent调用父; 父还可以通过$children访问子
vuex的使用共同状态
插槽内子向父传递数据通过v-bind指令被称为插槽prop

