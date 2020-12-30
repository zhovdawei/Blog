# GO安装和HelloWorld示例

### Window下的安装

****

**1.下载GO软件包**

[GO官网下载地址](https://golang.google.cn/dl/)

**2.下载Windows版本**

![20201228170950627](..\static\go\20201228170950627.png)

**3.环境变量**

GOROOT   E:\Go    // go安装目录

GOPATH   E:\go-work-place   // go工作空间

Path  ...E:\Go\bin...    

**4.CMD验证**

go version  查看版本
go env  查看环境参数

### 开发工具设置

---

选择**VSCODE**作为开发工具

**1.设置插件**

![20201228171931](..\static\go\20201228171931.png)

**2.设置GO变量**

```
# 开启go mod
$ go env -w GO111MODULE=on    
# 设置国内代理
$ go env -w GOPROXY=https://goproxy.cn,direct
```

**3.安装插件**

vscode ctrl+shift+p 快捷键打开设置搜索，搜索go:install ,选择GO：install/update Tools ，全选，确定。如果不能正常下载，可在第2步操作完成后，重启电脑，再次尝试。
![20201228171931](..\static\go\20201228214307.png)

**4.插件目录**

上面两步做完后，在GOPATH工作空间下多了两个目录bin和pkg。

![20201228171931](..\static\go\20201228214723.png)

### HelloWorld用例

----

**1.创建项目HelloWorld**

在GOPATH下创建名为HelloWorld的空项目。

![20201228171931](..\static\go\20201228220336.png)

**2.初始化项目**

~~~
$ cd HelloWorld
$ go mod init helloworld
~~~

此时HelloWorld初始化完成，并且目录下多了一个文件：go.mod.

**3.创建文件**

~~~go
package main

import (
	"fmt"
)

func main()  {
	fmt.Println("Hello world,Let`s go!")	
}
~~~

在HelloWorld目录下创建文件main.go文件，代码如上。

**4.运行文件**

~~~
D:\go-work-place\HelloWorld>go run main.go
Hello world,Let`s go!
~~~

**5.BUILD后运行**

~~~
D:\go-work-place\HelloWorld>go build

# HelloWorld下得到一个helloworld.exe文件
D:\go-work-place\HelloWorld>helloworld.exe
Hello world,Let`s go!
~~~





