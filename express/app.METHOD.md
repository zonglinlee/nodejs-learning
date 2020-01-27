http.METHODS提供了所有的请求方法数组，遍历封装所有的app.get/app.post等方法
```js
http.METHODS.forEach(method => {
    method = method.toLowerCase()
    app.[method] = function(path,handler){
        app.routes.push({
            method,
            path,
            handler
        })
    }
})
```