# promise

#### 1.什么是promise?

 console.dir(Promise)
 Promise是一个构造函数,身上有all,reject,resolve几个方法,prototype上有then,catch等方法

> Promise对象是一个代理对象(代理一个值),被代理的值再Promise对象创建时可能是未知的.它允许你为异步操作的成功和失败分别绑定相应的处理方法.
> 似的异步方法可以像同步方法一样返回值,但并不是立即返回最终执行结果,而是一个**能代表未来出现的结果的Promise对象**???

#### 2.promise怎么创建?
```js
var p = new Promise(function(resolve,reject)){
         //做异步操作
         setTimeout(()=>{
    	resolve('一些数据信息')
},10)                    
```

#### 3.promise的三种状态

promise是异步操作,所以只有操作结果才可以改变promise状态

> 01-pending : 待定
>
> 02-fulfilled : 已解决/已实现
>
> 03-rejected:已拒绝/未实现
>
> 状态改变:
>
> pending--->fulfiled  
> pending--->rejected

​                        