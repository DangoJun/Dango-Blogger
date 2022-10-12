# AJAX
就是使用js来发送请求和接受响应
## XMLHttpRequest
XMLHttpRequest是一个函数，挂在window之上，可以构造出一个对象，通过构造出来的实例实现发送和响应

## AJAX 的四个步骤
1. 创建一个XMLHttpRequest对象
2. 调用对象的open方法
3. 监听对象的onload&onerror事件
 -- 专业的前端会改用onreadystatechange事件
 -- 在事件处理函数里面操作CSS文件内容
4. 调用对象的send方法(发送请求)
 --具体代码参考MDN用CRM大法搞定   

## onreadystatechange 事件
有五个状态码
0. 请求为初始化
1. 服务器连接已建立
2. 请求已接受
3. 请求处理中
4. 请求已完成，响应已就绪 