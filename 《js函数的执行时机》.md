# 《js函数的执行时机》


## 为什么西面代码会打印出6个6

```
let i = 0
for(i = 0; i<6; i++){
  setTimeout(()=>{
    console.log(i)
  },0)
}
```
* 因为setTimeOut() 是一个异步函数 js的执行机制时单线程环境，当JS遇到异步函数的时候，会把异步函数插入到队列中等待，然后继续执行后面的代码，也就是接下来的循环
* 执行的过程for(i=0) ——> for(i=1) ——> for(i=2) for(i=3) ——> for(i=4) ——> for(i=5)——> for(i=6)（跳出循环）——>console.log(6)*6

 


## 写出让上面代码打印 0、1、2、3、4、5 的方法
```
for(let i = 0; i<6; i++){
  setTimeout(()=>{
    console.log(i)
  },0)
}
```


## 除了使用 for let 配合，还有什么其他方法可以打印出 0、1、2、3、4、5

1. 将i的变量驻留在内存中，当输出j时，引用的是外部函数的变量值i，i的值是根据循环来的，执行setTimeout时已经确定了里面的的输出了。
```
for (var i=1; i<=6; i++) {
    (function(j) {
        setTimeout(()=> {
            console.log( j );
        }, 0);
    })(i);
}
```
2. 还可以将setTimeout的定义和调用分别放到不同部分:
```
function timer(i) {
    setTimeout( ()=>{
        console.log( i ),
    }, 0);
}
for (var i=1; i<=6;i++) {
    timer(i);
}
```

 