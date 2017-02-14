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
