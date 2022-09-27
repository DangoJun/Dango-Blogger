# 《js对象的基本用法》

## 声明变量两种语法

```JavaScript
    var obj = new Object();
    var obj = {};
    let obj = new Object();
    let obj = {};
```
## 如何删除对象的属性
```JavaScript
    // 如果要删除对象的属性值可以直接将属性值设为空
    var obj = {name:'张三',age:18,gender:'男'}
    obj.name = '',//这样name的values就没有了
    // 使用delete删除属性
    delete obj.name //这样就删除了 name属性
```
## 如何查看对象的属性值
```JavaScript
    var obj = {name:'张三',age:18,gender:'男'}
    Object.keys(obj) // 查看所有的key值
    Object.Values(obj) // 查看所有的values值
    Object.entries(obj) // 查看所有属性的键值对以数组形式
```
## 如何修改或增加对象的属性
* 修改对象的属性
   ```JavaScript
   obj.name = 'xxx'
   obj.age = 20
   //或者
   obj['name'] = 'xx'
   obj['age'] = 22
   ```
* 增加对象的属性 
   ```JavaScript
   // 使用Object.assign批量增加
   Object.assign(obj,{x1:1,x2:2,x3:3})
   //直接增加
   obj.name = '张三' //如果存在name就是修改如果不存在就是添加
   //或者
   obj['国籍'] = '中国'
   ```

## 'name' in obj 和obj.hasOwnProperty('name')的区别
1. 'name' in obj  是判断 obj对象中是否有'name'这个属性包括自生属性和共有属性
2. obj.hasOwnProperty('name')  只判断自身属性中是否有'name'这个属性
