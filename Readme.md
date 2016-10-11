# Readme
### DOL开发环境配置
### 1. 在Ubuntu上安装必要的环境
`$	sudo apt-get update`

`$ 	sudo apt-get install openjdk-7-jdk`

如果提示apt-get需要root权限，可以使用命令
`$  sudo su`
进入root模式，之后按exit可以退出root模式。

### 2. 拷贝相关文件到Ubuntu
首先在虚拟机中使用命令

`$  mkdir dol`

在home文件夹中创建一个dol文件夹，然后将下载好的dol_ethz.zip文件在windows下解压，然后使用U盘拷贝到Ubuntu虚拟机的dol文件夹中。然后解压systemc-2.3.1.tgz并拷贝到home文件夹中，文件夹命名systemc-2.3.1。

### 3. 编译systemc
首先进入systemc-2.3.1文件夹并新建文件夹objdir
`$  cd systemc-2.3.1`

`$	mkdir objdir`

`$	cd objdir`

运行configure

`$	../configure CXX=g++ --disable-async-updates`


编译systemc:

`$  sudo make install`

查看编译完成的文件目录并记录当前工作路径

`$  ls`

`$  pwd`

如图：
![path1](http://ww2.sinaimg.cn/mw1024/9ccbff0dgw1f8oaxdoca9j20i304umzp.jpg)
### 4. 编译dol
首先进入dol文件夹，然后修改build_zip.xml文件，添加systemc位置信息（之前记录的工作路径）：
![addpath](http://ww3.sinaimg.cn/mw1024/9ccbff0dgw1f8oaxborycj20k002l0tu.jpg)
然后编译dol:
`$	ant -f build_zip.xml all`

编译成功会显示build successful。最后测试运行第一个例子：
进入build/bin/main并运行第一个例子:

`$	cd build/bin/main`

`$	ant -f runexample.xml -Dnumber=1`

成功结果如图：
![success](http://ww4.sinaimg.cn/mw1024/9ccbff0dgw1f8oaxccy9zj20c00bigpf.jpg)

### 5. 实验总结
这次的配置实验在步骤上来说复杂度并不高，但是需要在不同的Ubuntu环境下可能出现的错误也不一定相同。在配置时，我遇到的问题一个是update时权限不够，后来使用 `$ sudo su`获取管理员权限之后才能更新。另一个问题是JDK环境配置不生效，这里出现的原因是update时没有完全更新完毕，后面重新update后就生效了。










