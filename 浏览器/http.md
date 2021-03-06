<!--
 * @Author: qianqian.zhao
 * @Date: 2020-03-26 09:36:49
 * @LastEditors: qianqian.zhao
 * @LastEditTime: 2020-04-06 19:04:38
 * @Description: http相关
 -->
### http
是tcp／ip协议中应用层的超文本传输协议；
1. http是无状态的网络通信协议；每次请求结束都会关闭，再次请求是一个新的请求；
2. 明文传输，报文信息不加密
3. 通信双方的身份不进行验证
4. 客户端向服务端发请求的过程中，请求报文有被篡改的可能性

#### http的版本变化
1. http0.9 只能发送get请求，服务器只能返回html结构的数据
2. http1.0 
   1. 可以传输的方式增多
   2. 服务器返回的数据格式变化
   3. 增加了头部信息、状态码
   4. 每次tcp连接只能发送一个请求，所以性能差
   5. 请求头有一个connection:keep-alive 表示持久连接
3. http1.1
   1. 引入了“持久连接”，每个tcp连接可以被多个请求复用。
   2. 但是多个请求按次序进行，服务器处理完一个才处理下一个，称为“队头阻塞”
   3. 对于同一个域名，允许同时建立6个持久连接
   4. 针对“队头阻塞”，1、减少请求数；2、同时打开多个“持久连接”
4. http2.0 主要解决http1.1效率不高的问题
   1. 同一个持久连接中，服务器可以不按照次序返回，称为“多工”
5. http3.0 

#### http的get和post请求的区别

### http的状态码
1. 200
2. 300
3. 400
4. 500
   
### http的状态管理
使用cookie与session以及token进行状态管理

### http头部字段
#### 缓存相关
##### 请求体头
if-modified-since
if-no-match
##### 响应体头
Expires
cache-control

last-modified
ETag
#### 跨域相关
   cors跨域请求
   ##### 请求体头
   origin
   ##### 返回体头
   Access-control-Allow-Origin
   Access-control-Allow-Credentials

#### 连接相关
##### 请求体
connection：keep-alive
#### 状态有关
   ##### 请求头
   cookie
   ##### 返回体头
   setCookie

### https
https使用的是TLS协议
  #### https为何安全
### http与https的区别
