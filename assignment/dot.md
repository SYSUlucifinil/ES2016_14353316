##Lab2:DOL实例分析&编程

####任务1：修改example2，让square模块变成两个
实现方法：修改dol/examples/example2/example2.xml文件中的迭代次数，减少生成的square和connection模块，即是将文件中的N值修改为2，然后再编译运行example2：

`$ cd dol/build/bin/main`

`$ ant -f runexample.xml -Dnumber=2`

运行结果：

![example2](http://thumbnail0.baidupcs.com/thumbnail/1faabebf71f9caa8eb2758c47b9b5fec?fid=2520034666-250528-667100792946785&time=1476622800&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-YatZCb8%2F35pEvnUMoo3UWk07G6c%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=6723243034948996337&dp-callid=0&size=c710_u400&quality=100)

点图如下：

原点图：
![dot1](http://thumbnail0.baidupcs.com/thumbnail/871ef402aabc2704aff34daec4b2b646?fid=2520034666-250528-231096531337913&time=1476622800&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-PMqVNpkOigytS1nvY2S66S6Giq8%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=6723258888491311310&dp-callid=0&size=c710_u400&quality=100)


修改之后的点图：
![dot2](http://thumbnail0.baidupcs.com/thumbnail/e12c6d68c8a67701d0ea34a8d2f25c80?fid=2520034666-250528-380792957230698&time=1476622800&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-C6%2BlNhex73%2BrsDmm00%2FFs%2Fgu0Rc%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=6723312174830319699&dp-callid=0&size=c710_u400&quality=100)
#### 任务2：修改example1，使其输出3次方数
实现方法：在原来的实例中，这里输出的是一个数的平方，所以可以直接将原来的平方计算式修改为三次方计算，可以在dol/examples/example1/src/square.c文件中，将square_fire函数修改为：
![](http://thumbnail0.baidupcs.com/thumbnail/a204f5a76f72d59d0f689ce3e6c85b5a?fid=2520034666-250528-799122748694588&time=1476622800&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-jZ%2Fpud875%2B5BK%2B4sihn56SR40RI%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=6723388759478573856&dp-callid=0&size=c710_u400&quality=100)

修改完成后需要将在dol/build/bin/main文件夹中先删除上次实验编译生成的example1文件夹，然后再编译运行：

`$ ant -f runexample.xml -Dnumber=1`

运行结果如下：
![](http://thumbnail0.baidupcs.com/thumbnail/f66fbe3d9e518ff9827218dc231f5d2f?fid=2520034666-250528-615495592366890&time=1476622800&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-ZW8v55%2Fb%2BWPaagaHSowMglNK8eg%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=6723331361450928130&dp-callid=0&size=c710_u400&quality=100)

点图如下：

![](http://thumbnail0.baidupcs.com/thumbnail/a58d3f1129df5a466b6808cd7d69f0c4?fid=2520034666-250528-116175103425773&time=1476622800&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-fNRegMXlfrAHbW%2FQxV01nL9Tasw%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=6723343503108081110&dp-callid=0&size=c710_u400&quality=100)

