# NodeJS服务器Demo

Node js example demo

Demo地址：[https://github.com/ACommonChinese/NodeJSExampleDemo](https://github.com/ACommonChinese/NodeJSExampleDemo)

此为NodeJS服务器访问静态资源示例，使用方法：

1. 进入到目录webserver下，使用命行安装node\_modules：`npm i`
2. 编辑webserver/config/config.js的`hostname`和`port`
3. 开启node服务：`node app.js`
4. 把你的文档放入public中即可，比如在public下建目录yourDocs并在里面放入index.html, 则访问地址为：`xxx/yourDocs/index.html`

**注: **也可以使用pm2管理进程：`pm2 start app.js`, 或者使用nodemon

```
sudo cnpm i nodemon -g # 安装nodemon
nodemon app.js 
```

