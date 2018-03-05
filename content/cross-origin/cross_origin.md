## 解决跨域问题

～～～
Failed to load http://localhost:3001/: No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'http://localhost:3000' is therefore not allowed access.
～～～

- 加载失败，Cross origin 的意思是跨源头，也就是跨越， request  是请求的意思。

- Access-Control-Allow-Origin 访问-控制-允许-源头，用来规定我（服务器）的资源都允许哪些网站去使用，  默认情况只要跨域都不允许，但是可以通过这一项，来设置白名单。

- Header 指的是http头部

~~~
➜  my-note git:(master) ✗ curl -I localhost:3000

HTTP/1.1 200 OK
X-Powered-By: Express
Accept-Ranges: bytes
Cache-Control: public, max-age=0
Last-Modified: Sun, 04 Mar 2018 03:37:52 GMT
ETag: W/"636-161ef164e80"
Content-Type: text/html; charset=UTF-8
Content-Length: 1590
Vary: Accept-Encoding
Date: Sun, 04 Mar 2018 03:59:39 GMT
Connection: keep-alive
~~~

curl -I 得到的都是 http 响应头部，里面明显是没有 access-c 那个 header 的。

那我们解决方式是给加上这个 header


### 解决跨域问题的办法：


- 响应是由后端发出，所以要去该后端代码。 express 具体做法就是安装 cors 这个包

- https://baike.baidu.com/item/jsonp/493658?fr=aladdin