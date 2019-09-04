# NodeJS服务器搭建

官网：[http://nodejs.cn/](http://nodejs.cn/)

Node.js 是一个基于 Chrome V8 引擎的 JavaScript 运行环境。 
Node.js 使用了一个事件驱动、非阻塞式 I/O 的模型，使其轻量又高效。 

- 新建项目文件夹比如 MyNode
- 在文件夹内打开终端，运行 npm init , 一直回车或者填你想填的内容
- 在MyNode中新建文件如：app.js
- 安装express, 终端输入  npm i express --save
- 在app.js中写如下代码:

  ```javascript
  var express = require('express')
  var app = express()
  app.use(function(req, res, next) {
    res.end('hello world')
  })
  app.listen(8090, () => {
    console.log(`App listening at http://127.0.0.1:8090`)
  })
  ```

- 终端指令 node app.js启动服务器
- 浏览器中 <http://127.0.0.1:8090>访问服务器

安装时出现问题：npm err! cb() never called, 解决方法参见：[Here](https://www.alex-arriaga.com/issue-when-running-npm-install-npm-err-cb-never-called-solved/)

```javascript
node -v #check version
sudo npm cache clean -f #Clear your npm cache
npm install -g n #Install the latest version of the Node helper
sudo n stable #Tell the helper(n) to install the latest stable version of Node
npm install #install again
```