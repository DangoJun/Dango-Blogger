# dom 的基本以及核心的用法

  dom就是文档对象模型，通过获取每个元素对象，操作元素的样式，事件或者内容

##  创建元素
1. innerHTMl()
2. document.createElement('')
都可以进行元素的创建，createElement()创建元素可以使结构更加清晰
innerHTMl性能会更高

## 增加元素
1. appendChild
2. insertBefore
appendChild 可以在元素的尾部追加元素 insertBefore可以在元素的开头追加元素

## 删除元素
removeChild
删除某个元素

## 修改元素
1. 修改元素的属性：src href title 等等
2. 修改内容 innerHTML 和 innerTest等
3. 修改表单 value type disabled等
4. 修改样式 style className 等
   
## 查询元素
 直接获取元素对象
1. querySelector
2. querySelectorAll
 获取节点的方式    
3. parentNode 获取父级节点 ， children获取子节点对象
   previousElementSib获取上一个兄弟节点
  nextElementSib获取下一个兄弟节点

## 绑定事件
```
 let divs = document.querySelectorAll('div')
    divs[0].onclick = function(){
        alert('11');
        // 传统的解绑
        divs[0].onclick = null
    }
    divs[1].addEventListener('click',fn)
    function fn(){
        alert('1212');
        divs[1].removeEventListener('click',fn)
    }
```
