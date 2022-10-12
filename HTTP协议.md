# HTTP
超文本传输协议,详细规定了浏览器和万维网服务器之间相互通讯的规则
一种规定和规则

## 请求报文
重点是格式与参数
```
行     POST  / 参数  / HTTP/1.1 版本
头     Host: baidu.com
       Cookie: name=baidu
       Content-type : xxxxxxxxx
       User-Agent: chrome 83
空行
体     username = admin&password=admin
```

## 响应报文
```
行      HTTP/1.1   200  OK  (版本和状态码和状态)
头      Content -Type :text/html;charset=utf-8
        Content-length :2048
        Content-encoding:gzip

空行    
体      <html>
            <head>
                <body>
                    <h1>Hello World</h1>
                </body>
            </head>

        </html>
```
* 404
* 403
* 401
* 500
* 200

