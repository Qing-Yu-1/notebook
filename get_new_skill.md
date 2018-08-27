
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
sudo -S netease-cloud-music


