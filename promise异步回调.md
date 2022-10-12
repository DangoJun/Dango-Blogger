# 异步
如果一个函数的返回值处于一下代码中就是异步函数
1. setTimeout
2. XMLHttpRequest
3. addEventListener

return new Promise((resolve,reject)=>{})