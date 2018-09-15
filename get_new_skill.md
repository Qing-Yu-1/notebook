
##################################################################7.19<Br/>
# github chrome插件
安装插件：Octotree 链接：https://github.com/buunguyen/octotree<Br/>
安装插件：github-plus　可以方便在github上下载单个文件<Br/>
其他有用的针对github的工具，链接地址：https://blog.csdn.net/poem_of_sunshine/article/details/77894438<Br/>
# 百度网盘下载器
百度网盘下载器：bnd 链接地址：https://github.com/Qing-Yu-1/baidu-netdisk-downloaderx<Br/>　
			　通过 Cookie [BDUSS] 登录，无需担心密码泄漏<Br/>
			发布包：https://share.weiyun.com/57zViCm<Br/>
			通过黑客派网站获取下载积分，https://hacpai.com/<Br/>			
发现google的日历可以替代日计划安排表<Br/>
vlc播放功能还是很强大的，播放列表很好用<Br/>
################################################################7.23<Br/>
# grip
`grip`可以在浏览器中查看git中的md格式的文档,然后用浏览器的pdf打印功能转换为PDF文件<Br/>
`sudo pip install grip`<Br>
`grip ssd.md(文件) `<Br>

git上的md页面可以直接通过浏览器打印成pdf格式<Br/>

# 百度云盘上传：bypy
https://github.com/houtianze/bypy/blob/master/README.md<Br/>
由于百度PCS API权限限制，程序只能存取百度云端/apps/bypy目录下面的文件和目录。我们可以通过<Br/>
`bypy list`显示在云盘（程序的）根目录下文件列表<Br/>
把当前目录同步到云盘：`bypy upload`<Br/>
把云盘内容同步到本地来： <Br/>
```
bypy downdir /
```
比较本地当前目录和云盘（程序的）根目录（个人认为非常有用）：<Br/>
```
bypy compare
```
# linux apt-cache使用方法
apt-cache是linux下的一个apt软件包管理工具，它可查询apt的二进制软件包缓存文件。APT包管理的大多数信息查询功能都可以由apt-cache命令实现,通过apt-cache命令配合不同的子命令和参数的使用,可以实现查找,显示软件包信息及包依赖关系等功能.<Br/>

1> `apt-cache show package_name`<Br/>
显示指定软件包的信息，包括版本号，安装状态和包依赖关系等.<Br/>
2> `apt-cache search package_name`<Br/>
搜索软件包，可以按关键字查找软件包,通常用于查询的关键字会使用软件包的名字或软件包的一部分.
# apt-key命令
语法:`apt-key(参数)`<Br/>
参数：APT密钥操作指令。<Br/> 
实例:
```
apt-key list          #列出已保存在系统中key。
apt-key add keyname   #把下载的key添加到本地trusted数据库中。
apt-key del keyname   #从本地trusted数据库删除key。
apt-key update        #更新本地trusted数据库，删除过期没用的key。
```
`7.25`
```
df-h 
```
查看磁盘的剩余空间
```
sudo fdisk -l
```
查看整个硬盘的分区情况<Br/>
激活ros环境<Br/>
```
~/catkin_ws2/devel/setup.sh
```
新建空文件夹：<Br/>
```
touch a.txt
>a.txt
```
在anaconda３的machineLearning环境下查看pip的版本，可以使用pip install 安装python包
```
~/software/anaconda3/envs/machineLearning/lib/python3.6/site-packages$ pip -V
```
安装一个 Debian 软件包，如你手动下载的文件。
```
sudo dpkg -i <package.deb>
```
打开网易云音乐
```
sudo -S netease-cloud-music
```
### 删除软件

方法一、如果你知道要删除软件的具体名称，可以使用<br/>
```
sudo apt-get remove --purge 软件名称  
sudo apt-get autoremove --purge 软件名称 
```
### 在ubuntu下basket note pads则可以媲美onenote<br/>
安装方法:<br/>
```
sudo apt-get install basket
```
### xz压缩文件方法或命令
要压缩的文件<br/>
```
xz -z 
```
如果要保留被压缩的文件加上参数 -k ，如果要设置压缩率加入参数 -0 到 -9调节压缩率。如果不设置，默认压缩等级是6.<br/>
xz解压文件方法或命令<br/>
```
xz -d #要解压的文件
```
创建tar.xz文件：只要先 `tar cvf xxx.tar xxx/` 这样创建xxx.tar文件先，然后使用 `xz -z xxx.tar` 来将 xxx.tar压缩成为 xxx.tar.xz<br/>
解压tar.xz文件：先 `xz -d xxx.tar.xz` 将 xxx.tar.xz解压成 xxx.tar 然后，再用 `tar xvf xxx.tar`来解包。<br/>
### tar.gz安装与卸载
tar.gz源代码包安装方式：
1、找到相应的软件包，比如soft.tar.gz，下载到本机某个目录；<br/>
2、打开一个终端，使用命令：su –转换成root用户；<br/>
3、`cd soft.tar.gz`所在的目录；<br/>
4、`tar -xzvf soft.tar.gz` //一般会生成一个soft目录<br/>
5、`cd soft`<br/>
6、`./configure --prefix=/usr/local/soft`(指定安装目录)<br/>
7、`make`<br/>
8、`make install`<br/>
卸载：用cd 命令进入编译后的软件目录，即安装时的目录<br/>
执行反安装命令：make uninstall或 手动删除<br/>
### A Primer on Using LaTeX in Jupyter Notebooks
http://data-blog.udacity.com/posts/2016/10/latex-primer/

### 有道云笔记网页版markdown插入图片
１．建议一个专门存放图片的文件夹<br/>
２．在这个文件夹中建立一个普通笔记，将图片上传（直接粘贴）到这个页面<br/>
３．分享这个页面，查看分享，在弹出的新页面中找到对应的图片，直接右键，选择复制该图片的地址<br/>
４．在markdown的界面中输入｀![](图片地址）｀就ＯＫ了<br/>
5.如果不差钱，可以开通会员，直接上传
### 有道云笔记网页版markdown 插入公式
插入公式示例：
```
｀｀｀math
E = mc^2

\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}

P_1

a^2
｀｀｀
```
格式和　MathJax: LaTeX 差不多，只不过将$$ 换成了：
```
｀｀｀math
｀｀｀
```
MathJax: LaTeX<br/>
https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference
### 护眼软件　redshift redshif-gtk
https://github.com/jonls/redshift
### 闹钟
打开 Ubuntu 终端，我们要安装的就是那个 `alarm-clock-applet`
### 手机翻墙软件
https://github.com/XndroidDev/Xndroid





