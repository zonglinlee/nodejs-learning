# [Express](https://expressjs.com/)
Express is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls
## app方法
express 中 路由处理函数的顺序很重要,它们会根据调用顺序push到一个数组中，再遍历绑定的请求处理函数，如果数组中前面的请求处理函数匹配上了url.pathname，则后续的就不会再匹配了。

- app.all(path,callback) 匹配所有请求方法(get/post/delete等等)

## [中间件](https://expressjs.com/en/guide/using-middleware.html)
Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

Middleware functions can perform the following tasks:

- Execute any code.
- Make changes to the request and the response objects.
- End the request-response cycle.
- Call the next middleware function in the stack.

If the current middleware function does not end the request-response cycle, it must call next() to pass control to the next middleware function. Otherwise, the request will be left hanging.



