# jQuery 的基本用法
jQuery 是js目前寿命最长的一个库里面封装了许许多多的方法，可以更方便的操作dom
jQuery 可以跨浏览器兼容 ，并且体积很小 而且开源免费


### jQuery 的入口方法
```
$(document).ready(function(){
    // 等待dom加载完成后执行
})
```
```
$(function(){
      // 等待dom加载完成后执行
})
```
 这两个方法是等价的

### jQuery  和  $
$  是 jQuery 的别称    $是jQuery中的顶级对象相当于js中的window


### dom 和 jQuery 对象的转换

```
// dom 对象 转jQuery
let mydiv  = document.querySelector('div')
$(mydiv);  // 这样 dom对象就转换成了 jQuery对象了

// jquery 转换 dom
$('div')[0];
$('div').get(0)
// 以上两种方式都可以转换
```

### 筛选选择器
1. :first $('li:first')  获取第一个li
2. :last $('li:last')  获取最后一个li
3. :eq(index) $('li:eq(index)')  获取对应下标的li
4. :odd $('li:odd')  获取奇数的li(索引号)
5. :even $('li:even')  获取偶数的li(索引号)
6. parent() 选择父元素
7. children(selector) 子元素  
8. siblings(selector) 兄元素  选取所有兄弟不包含自身
9. nextAll() 选取 当前元素之后的所有同级兄弟
10. prevtAll() 选取 当前元素之前的所有同级兄弟
11. $('div:first').hasClass('current')  // 如果有返回true 没有返回false

### 基本api
1. show() 显示元素
2. hide() 隐藏元素
3. index() 获取元素下标
