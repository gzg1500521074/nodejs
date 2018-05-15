# 第四课：事件 

## 任务 1：阅读 Node.js API 资料  

- [EventEmitter API 资料](http://nodejs.cn/api/events.html)  

## 任务 2：

要求：
- 创建 08-event 目录  
- 编写 01-event-emitter.js 脚本，发出自定义事件，并写事件处理函数  

## 任务 3：

要求：
- 编写 02-dog.js 以及 02-play-dog.js 脚本  
- Dog 类原型继承 EventEmitter 类  
- 在 Dog 类中，实现 engery 能量私有数据成员的逻辑
- 在 Dog 类中，用构造函数对私有数据 energy 进行初始化
- 在 Dog 类中，bark 事件跟 energy 数据进行逻辑关联，bark 一次 energy 数值减一
- 在 Dog 类中，energy 数值为零时，不发出 bark 事件
- 02-play-dog.js 实现多个 Dog 的对象，对多个对象采用相同的 bark 事件处理机制  

## 任务 4：

要求：
- 编写 03-radio.js 以及 03-listen-radio.js  
- radio 类 util 的 inherits 方法继承 EventEmitter 类  
- radio 类发出 play 事件和 stop 事件  
- 03-listen-radio.js 脚本，实例化 radio 对象，并处理 play 和 stop 事件  

## 任务 5：

要求：
- 编写 04-mixing-event-emitter.js 脚本  
- 实现一个 musicPlayer 类，拷贝 EventEmitter 原型中的方法  
- musicPlayer 类，发出两个事件：play 和 stop  
- 在 musicPlayer 的实例中，编写两个事件的事件处理代码  

## 任务 6：

要求：
- 编写 05-error.js 脚本  
- 在 04-mixing-event-emitter.js 脚本的基础上实现  
- 在 musicPlayer 类中发出 error 事件，在 musicPlayer 的实例上进行异常捕获，或者在进程级别上进行异常捕获  
