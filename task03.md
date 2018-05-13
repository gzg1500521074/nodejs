# 第三课：全局（下）

## 任务 1：阅读 Node.js API 资料  

- [Buffer API 资料](http://nodejs.cn/api/buffer.html)  

## 任务 2：Buffer 基本操作

要求：
- 创建 06-buffer 目录  
- 编写 01-basic.js 脚本  
- 实例化一个 buffer 对象 buf1，缓冲区的大小是 256 字节，初始化第一个字节为零，控制台打印 buf1 的长度和内容  
- 通过循环初始化 buf1 的每个字节，每个字节比上个字节大 1，控制台打印 buf1 的内容  
- 对 buf1 做切片操作，取出后 10 个字节，存放到 buf2 中，控制台打印 buf2 的内容和长度   
- 对 buf2 做填充操作，所有字节填充为零，控制台打印 buf2 的内容
- 用数组（数组内容随意）初始化 buf3，控制台打印 buf3 中的内容和长度  
- 用字符串（字符串内容随意）初始化 buf4，控制台打印 buf4 中的内容和长度，打印 buf4 字符串  
- 将 buf4 的内容复制到 buf3 中，打印复制后的 buf3 内容和长度，打印 buf3 字符串  

## 任务 3：Buffer 编码

要求：
- 编写 02-encode.js 脚本  
- 阅读 [basic authentication 资料](https://en.wikipedia.org/wiki/Basic_access_authentication)  
- 从命令行参数获取登录网站的用户名和密码信息  
- 命令行参数的格式：cmd user_name password  
- 命令行参数不正确时，提示用户命令行参数的正确格式
- 在控制台打印用户名和密码信息  
- 将用户名和密码信息拼接成一个字符串，用冒号（:）分割
- 将拼接后的字符串转化成 base64 编码，并打印在控制台上  

## 任务 4：Buffer 解码

- 编写 02-decode.js 脚本  
- 从命令行参数获取用户名和密码信息的 base64 编码字符串  
- 命令行参数的格式：cmd base64_string  
- 命令行参数不正确时，提示用户命令行参数的正确格式
- 将 base64 编码的字符串转换成 utf8 编码的字符串
- 将还原后的用户名和密码信息打印在控制台上  
- 还原信息不正确时，请提示错误信息

## 任务 5：Buffer 实现 Data URI

要求：
- 编写 03-data-uri.js 脚本  
- 阅读 [data URI scheme 资料](https://en.wikipedia.org/wiki/Data_URI_scheme)  
- 执行 `wget http://sample.wangding.in/nodejs/nodejs-logo.bmp` 下载 nodejs-logo.bmp 测试图片  
- 执行 `wget http://sample.wangding.in/nodejs/qr-code.jpg` 下载 qr-code.jpg 测试图片  
- 执行 `wget http://sample.wangding.in/nodejs/book.png` 下载 book.png 测试图片  
- 从命令行参数获取图片文件名  
- 命令行参数的格式：cmd file_name  
- 命令行参数不正确时，提示用户命令行参数的正确格式  
- 命令行参数的图片文件不存在时，提示错误信息  
- 把图片数据生成 data URI 格式的数据  
- 把 data URI 数据打印到控制台  
- 把 data URI 数据嵌入到 HTML 页面中  
- 创建一个 HTTP 服务，监听 8080 端口  
- 浏览器请求 HTTP 服务的 URL 地址时，得到嵌入图片数据的 HTML 页面  

提示：
- 文件操作需要导入 fs 模块： `const fs = require('fs');`
- 读取文件数据可以使用 readFileSync 方法：`var data = fs.readFileSync(fileName);`
- 同步读取文件时，如果文件不存在会抛出异常，可以使用 `try-catch` 捕获异常
- 获取文件扩展名，需要导入 path 模块：`const path = require('path');`
- 获取文件扩展名使用 path 模块的 extName 方法：`var ext = path.extName(fileName);`

## 任务 6：Buffer 读取位图信息

要求：
- 编写 04-bmp-info.js 脚本  
- 阅读 [BMP 文件格式资料](https://en.wikipedia.org/wiki/BMP_file_format)  
- 从命令行参数获取图片文件名  
- 命令行参数的格式：cmd file_name  
- 命令行参数不正确时，提示用户命令行参数的正确格式  
- 命令行参数的图片文件不存在时，提示错误信息  
- 获取图片的宽度、高度和颜色深度三个信息，并打印在控制台上  

## 任务 7：Buffer 写入位图文件

要求：
- 编写 05-bmp-write.js 脚本  
- 从命令行参数获取图片文件名  
- 命令行参数的格式：cmd file_name  
- 命令行参数不正确时，提示用户命令行参数的正确格式  
- 写一个 16 * 16 像素，颜色深度为 32 位的位图文件  
- 位图的所有像素为红色  

## 任务 8：阅读 Node.js API 资料

- [module API 资料](http://nodejs.cn/api/modules.html)  

## 任务 9：使用第三方模块

要求：
- 创建 07-module 目录  
- 编写 01-third-module.js 脚本  
- 导入 date-now 模块  
- 调用 date-now 模块的 now 方法，在控制台打印 now 的运行结果  
- 安装 date-now 模块，运行程序  
- 创建 package.json 文件，用 npm install module-name -S 安装模块  
- 查看 package.json 文件中的依赖项  

## 任务 10：创建并使用模块，导出变量

要求：
- 编写 02-export-var.js 脚本
- 导出变量 Math.PI
- 打印 module 信息  
- 编写 02-main.js 脚本
- 导入上面的模块
- 测试模块的接口  

## 任务 11：创建并使用模块，导出函数

要求：
- 编写 02-export-function.js 脚本  
- 导出 circle 函数  
- 函数的入口参数是圆的半径  
- circle 函数返回一个对象  
- 对象中有两个成员函数，分别计算：圆的面积和周长  
- 打印 module 信息  
- 编写 02-main.js 脚本
- 导入上面的模块
- 测试模块的接口  

## 任务 12：创建并使用模块，导出对象

要求：
- 编写 02-export-object.js 脚本  
- 导出 Circle 类  
- 函数的构造函数，入口参数是圆的半径  
- 类有三个公开方法，分别计算圆的直径、面积和周长  
- 打印 module 信息  
- 编写 02-main.js 脚本
- 导入上面的模块
- 测试模块的接口  

## 任务 13：管理一组相关模块

要求：
- 编写 03-export-all.js 脚本
- 导入上面定义的三个模块
- 暴露出一个对象  
- 编写 03-main.js 脚本
- 对 03-export-all.js 脚本进行测试  
