<!--
 * @Author: qianqian.zhao
 * @Date: 2020-03-26 16:19:18
 * @LastEditors: qianqian.zhao
 * @LastEditTime: 2020-03-26 18:34:13
 * @Description: promise
 -->

### 宏任务
  1. settimeout

### 微任务
  1. promise的resolve以及reject

### promise
  1. promise的状态一经改变就不会再变
  2. promise的.then和.catch可以多次调用，每次调用都直接拿到已经存储的值
  3. promise可以链式调用
  4. promise执行.then以及.catch都会返回一个新的promise对象,返回的任何一个非peomise的值都会被包裹成promise对象
  5. .then或者.catch返回的值不可以是promise本身，否则会循环 !!!
  6. 链式promise要等前一个微任务执行之后才会将后面的任务加到微任务列表
  7. .finally一直都会执行，而且会返回前一个promise，不会产生新的promise