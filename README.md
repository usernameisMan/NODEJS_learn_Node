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

#### Events
  事件对象
     
#### Stream
  数据流

#### Modules
  模块机制

#### Errors
  错误捕获机制
