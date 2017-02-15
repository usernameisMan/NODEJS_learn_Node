# 核心概念 
### Timers /Buffer / Events / Stream / Modules / Errors / fs


#### fs
  文件操作
  ```js
    // 读取文件
    fs.readFile(PATH,encoding,FUN(err,data));
    // 写入文件
    fs.writeFile(PATH,FUN(err));
    // 删除文件
    fs.fs.unlink(PATH,FUN(err));
    // 修改文件名字
    fs.rename(PATH,toName,FUN(err));
    // 查看文件状态
    fs.stat(PATH, FUN(err, stat));
    // 判断文件是否存在
    fs.exists(PATH, FUN(exists);
  ```
#### Timers
  定时器

#### Buffer
  数据缓冲
  ```js
    //Buffer(对象),buf(实例)
    //判断对象是否为 Buffer 返回 Boolean
    Buffer.isBuffer(obj);
    //判断 Buffer 对象编码 返回 Boolean
    Buffer.isEncoding(encoding);
    //返回 buf 在字节数上分配的内存量
    buf.length
    //一个参数的时候
    //返回string在实例中第一次出现的位置
    //第二个是起始位置
    //第三个是编码
    buf.indexOf(STRING,[byteOffset],[encoding])
    //bug拷贝进到目标对象
    buf.copy(targetObj,[targetObjStart],[sourceStart],[sourceEnd])
  ```

#### Events
  事件对象
     
#### Stream
  数据流

#### Modules
  模块机制

#### Errors
  错误捕获机制
  
#### HTTP

```js
     var http = require('http');
     var querystring = require('querystring');
     var options = {
             host: 'xxx', // 这个不用说了, 请求地址
             port:80,
             path:path, // 具体路径, 必须以'/'开头, 是相对于host而言的
             method: 'GET', // 请求方式, 这里以post为例
             headers: { // 必选信息, 如果不知道哪些信息是必须的, 建议用抓包工具看一下, 都写上也无妨...
                 'Content-Type': 'application/json'
             }
         };
         http.get(options, function(res) {
             var resData = "";
             res.on("data",function(data){
                 resData += data;
             });
             res.on("end", function() {
                 callback(null,JSON.parse(resData));
             });
         })
```
POST
```js
    var http = require('http');
    var querystring = require('querystring');
    //json转换为字符串
    var data = querystring.stringify({
        id:"1",
        pw:"hello"
    });
    var options = {
        host: '115.29.45.194',
    //    host:'localhost',
    //    port: 14000,
    //    path: '/v1?command=getAuthenticode',
        path:'/callme/index.cfm/userService/command/getAuthenticode/',
        method: 'POST',
        headers: {
            'Content-Type': 'application/x-www-form-urlencoded',
            'Content-Length': Buffer.byteLength(data)
        }
    };

    var req = http.request(options, function(res) {
        res.setEncoding('utf8');
        res.on('data', function (chunk) {
            console.log("body: " + chunk);
        });
        res.on('end',function(chunk){
            console.log("body: " + chunk);
        })
    });
    req.write(data);
    req.end();
```
