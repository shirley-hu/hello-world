1. 解决"'pip' 不是内部或外部命令，也不是可运行的程序或批处理文件"

添加至环境变量 C:\Users\jennifer.zheng\AppData\Local\Continuum\anaconda3\Scripts

C:\Users\jennifer.zheng\AppData\Local\Continuum\anaconda3\Library\bin

2. 环境变量配置内容。在Path后面追加一下内容(Path： 不要复制进去)

Path:     ;C:\python;C:\Python\Scripts

3. Spyder用conda 来进行安装，不要用pip 来安装。在已经安装了anaconda的情况下，pip安装有可能会损坏原文件。

打开Terminal，输入代码：

conda update spyder

然后再出现的Y/s中选择Y。

4.遇到问题：输入conda时显示 command not found。

解决办法：

1）在terminal中输入：

export PATH="/Users/username/anaconda/bin:$PATH"

(此处的/Users/username/anaconda/bin 指bin文件所在的位置。如果不知道的话，可以通过点击finder中的应用程序，找到anaconda，右边点击显示包文件（原件），然后找到bin文件夹，右键，点击显示简介来查看具体目录)

2）成功输入后，再输入以下代码，确保以后每次启动都能使用conda命令。

source ~/.zshrc

Bash命令稍有不同，可自行搜索。
（版权声明：本文为CSDN博主「Ericchen0804」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/Ericchen0804/article/details/79824772）

