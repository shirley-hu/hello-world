### 1. 报错"'pip' 不是内部或外部命令，也不是可运行的程序或批处理文件"
添加至环境变量 C:\Users\jennifer.zheng\AppData\Local\Continuum\anaconda3\Scripts
C:\Users\jennifer.zheng\AppData\Local\Continuum\anaconda3\Library\bin

### 2. 环境变量配置内容。在Path后面追加以下内容
Path:     ;C:\python;C:\Python\Scripts     (Path： 不要复制进去)

### 3. 用conda安装Spyder
不要用pip安装。在已经安装了anaconda的情况下，pip安装有可能会损坏原文件。
打开Terminal，输入代码：
conda update spyder
然后再出现的Y/s中选择Y。

### 4. 输入conda时显示command not found。
解决办法：
1）在terminal中输入：
export PATH="/Users/username/anaconda/bin:$PATH"
(此处的/Users/username/anaconda/bin 指bin文件所在的位置。如果不知道的话，可以通过点击finder中的应用程序，找到anaconda，右边点击显示包文件（原件），然后找到bin文件夹，右键，点击显示简介来查看具体目录)

2）成功输入后，再输入以下代码，确保以后每次启动都能使用conda命令。
source ~/.zshrc
Bash命令稍有不同，可自行搜索。
版权声明：本文为CSDN博主「Ericchen0804」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/Ericchen0804/article/details/79824772

### 5. ERROR conda.core.link:_execute_actions(337):
An error occurred while installing package 'defaults::tqdm-4.39.0-py_0'.
CondaError: Cannot link a source that does not exist. C:\Users\Dell\Anaconda3\Scripts\conda.exe
Running `conda clean --packages` may resolve your problem.
Attempting to roll back.

解决方法：1) Try doing running: 'conda install tqdm -f' first.
2) I found that it helps to do a
conda update conda
before doing any other upgrade/install operations
3) Run command :
conda config --add pinned_packages defaults::conda

### 6. 使用国内的镜像网站：
http://pypi.doubanio.com/simple/
大家可以打开看一下该网站，几乎包含所有的常见包，当然了，大家可以按照字母顺序找一下里面是否包含自己即将要安装的包，一般来说是有的。

对应的命令行就是
pip install 安装包名字  -i http://pypi.doubanio.com/simple/ --trusted-host pypi.doubanio.com
对应到我们这里要安装tensorflow便是：
pip install tensorflow  -i http://pypi.doubanio.com/simple/ --trusted-host pypi.doubanio.com

使用镜像网站吧，这次使用清华的：给anaconda添加该镜像网站：
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --set show_channel_urls yes
可以输入2次
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
这样该网站就置顶了
————————————————
版权声明：本文为CSDN博主「weixin_42001089」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_42001089/article/details/84403842版权声明：本文为CSDN博主「weixin_42001089」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_42001089/article/details/84403842

