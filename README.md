# detail-about-cookie-and-session
## 什么是session和cookie
> session和cookie是用来判断是否是同一个人给服务器发送的请求
## 为什么要用他们？
> 因为HTTP是无状态的，他不知道是谁向它发送的请求
## 浏览器是怎么种cookie的？
> 客户端向服务器发送请求，服务器会给他生成一个唯一标识的ID，并在返回结果response-headers中有一个set-cookie字段
> 浏览器看到set-cookie这个字段就种下了cookie
## 服务器怎么拿到cookie？
> 浏览器种完cookie后会在向服务器发送请求时将这个cookie带过去，服务器就拿到了这个cookie
## 浏览器关闭和不发送请求时，session消失
> 因为session没有设置时间有效期，所以当前会话关闭session消失
> 服务器会给session定一个时间，当再次发送请求时，服务器会把当前时间和设定的时间做对比，如果超时则session失效
