
##################################################################7.19<br/>
# github chrome插件
安装插件：Octotree 链接：https://github.com/buunguyen/octotree<br/>
安装插件：github-plus　可以方便在github上下载单个文件<br/>
其他有用的针对github的工具，链接地址：https://blog.csdn.net/poem_of_sunshine/article/details/77894438<br/>
# 百度网盘下载器
百度网盘下载器：bnd 链接地址：https://github.com/Qing-Yu-1/baidu-netdisk-downloaderx<br/>　
			　通过 Cookie [BDUSS] 登录，无需担心密码泄漏<br/>
			发布包：https://share.weiyun.com/57zViCm<br/>
			通过黑客派网站获取下载积分，https://hacpai.com/<br/>			
发现google的日历可以替代日计划安排表<br/>
vlc播放功能还是很强大的，播放列表很好用<br/>
################################################################7.23<br/>
# grip
`grip`可以在浏览器中查看git中的md格式的文档,然后用浏览器的pdf打印功能转换为PDF文件<br/>
`sudo pip install grip`<br>
`grip ssd.md(文件) `<br>

git上的md页面可以直接通过浏览器打印成pdf格式<br/>

# 百度云盘上传：bypy
https://github.com/houtianze/bypy/blob/master/README.md<br/>
由于百度PCS API权限限制，程序只能存取百度云端/apps/bypy目录下面的文件和目录。我们可以通过<br/>
`bypy list`显示在云盘（程序的）根目录下文件列表<br/>
把当前目录同步到云盘：`bypy upload`<br/>
把云盘内容同步到本地来： <br/>
```
bypy downdir /
```
比较本地当前目录和云盘（程序的）根目录（个人认为非常有用）：<br/>
```
bypy compare
```
# linux apt-cache使用方法
apt-cache是linux下的一个apt软件包管理工具，它可查询apt的二进制软件包缓存文件。APT包管理的大多数信息查询功能都可以由apt-cache命令实现,通过apt-cache命令配合不同的子命令和参数的使用,可以实现查找,显示软件包信息及包依赖关系等功能.<br/>

1> `apt-cache show package_name`<br/>
显示指定软件包的信息，包括版本号，安装状态和包依赖关系等.<br/>
2> `apt-cache search package_name`<br/>
搜索软件包，可以按关键字查找软件包,通常用于查询的关键字会使用软件包的名字或软件包的一部分.
# apt-key命令
语法:`apt-key(参数)`<br/>
参数：APT密钥操作指令。<br/> 
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
查看整个硬盘的分区情况<br/>
激活ros环境<br/>
```
~/catkin_ws2/devel/setup.sh
```
新建空文件夹：<br/>
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
### 查看已安装软件的位置和信息（通过apt-get的方式）
apt-get install安装目录是包的维护者确定的，不是用户
```
dpkg -L 软件名
```
### 删除没用的deb包
`/var/cache/apt/archives`是apt-get方式下载的deb包
可以通过`sudo apt-get clean`删除deb包

### 动态链接库的配置问题
相关链接：https://blog.csdn.net/farmwang/article/details/72877810
编辑文件，把库的路径添加到ld.so.conf文件中
```
sudo vim /etc/ld.so.conf
```
配置完成后，执行一下命令，是文件立即生效
```
$ sudo ldconfig
```
### Linux下环境变量配置方法梳理（.bash_profile和.bashrc的区别）
`~/.bash_profile`: 每个用户都可使用该文件输入专用于自己使用的shell信息,当用户登录时,该文件仅仅执行一次!默认情况下,他设置一些环境变量,执行用户的.bashrc文件(??).<br/>
`~/.bashrc`: 该文件包含专用于你的bash shell的bash信息,当登录时以及每次打开新的shell时,该该文件被读取.<br/>
`/etc/profile`: 此文件为系统的每个用户设置环境信息,当用户第一次登录时,该文件被执行.并从/etc/profile.d目录的配置文件中搜集shell的设置.<br/>
`~/.bashrc`: 该文件包含专用于你的bash shell的bash信息,当登录时以及每次打开新的shell时,该该文件被读取.<br/>
`~/.bash_logout`: 当每次退出系统(退出bash shell)时,执行该文件.<br/>
另外,`/etc/profile`中设定的变量(全局)的可以作用于任何用户,而`~/.bashrc`等中设定的变量(局部)只能继承`/etc/profile`中的变量,他们是"父子"关系.<br/>
```
KETTLE_HOME=/path/to/dir
export KETTLE_HOME
```
注意：配置好环境变量后，要记得export输出这个变量，否则如下source后无效！
[app@test ~]$ source .bashrc //使之生效
### 安装tmux
tmux（github)
https://github.com/tmux/tmux

linux 下安装软件tar.gz, rpm,deb的方法:
http://blog.chinaunix.net/uid-23781137-id-3455554.html
```
第一部分：搞定.tar.gz

　　1.首先，使用tar -xzvf来解开这个包，如：
　　#tar -xzvf apache_1_3_6_tar.gz
　　这样就会在当前目录中创建了一个新目录(目录名与.tat.gz包的文件名类似），用来存放解压了的内容。如本例中就是apache_1.3.6

　　2.进入这个目录，再用ls命令查看一下所包含的文件，如：
　　#拟定cd apache_1.3.6
　　#ls
　　你观察一下这个目录中包含了以下哪一个文件：configure、Makefile还是Imake。
1）如果是configure文件,就执行：
　　#./configure 
　　#make
　　#make install
2）如果是Makefile文件,就执行：
　　#make
　　#make install
3）如果是Imake文件,就执行：
　　#xmkmf
　　#make
　　#make install
```
https://www.jianshu.com/p/cece3a18723d(遇到的问题）
安装两个依赖包
```
tmux depends on libevent 2.x. Download it from:

	http://libevent.org

It also depends on ncurses, available from:

	http://invisible-island.net/ncurses/

To build and install tmux from a release tarball, use:

	$ ./configure && make
	$ sudo make install
```
```
tmux can use the utempter library to update utmp(5), if it is installed - run
configure with --enable-utempter to enable this.

To get and build the latest from version control:

	$ git clone https://github.com/tmux/tmux.git
	$ cd tmux
	$ sh autogen.sh
	$ ./configure && make
```
Tmux: Error While Loading Shared Libraries: libevent-2.0.so.6（遇到的错误）

```
export DIR="$HOME/local"
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$DIR/lib
./configure --prefix=$DIR CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib"
make
make install
```
https://blog.csdn.net/m0_37170593/article/details/78892913(关于第三行的解释`./configure ...`）<br/>
`eport LD_LIBRARY_PATH`的使用<br/>
`LD_LIBRARY_PATH`Linux环境变量名，该环境变量主要用于指定查找共享库（动态链接库）时除了默认路径之外的其他路径。<br/>
https://www.cnblogs.com/wainiwann/p/4210343.html
'.zshrc'需要添加：
```
export DIR="$HOME/local"
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$DIR/lib
```
以便每次运行zsh时，就把LD_LIBRARY_PATH的路径添加到当前shell中。
### 查看当前shell的值
单独查看PATH环境变量
```
echo $PATH
```
可用 `export` 命令查看PATH值
### 使用which
which命令的原理：在PATH变量指定的路径中，搜索某个系统命令的位置，并且返回第一个搜索结果。也就是说，使用which命令，就可以看到某个系统命令是否存在，以及执行的到底是哪一个位置的命令。
### tmux内的复制和粘贴
http://jasonwryan.com/blog/2011/06/07/copy-and-paste-in-tmux/
```
Ctrlt+a,Escape   # enter copy mode
# move cursor to the start or end of the desired text string
v                        # to activate highlighting
# move cursor to cover the requisite string
y                        # to capture the string
q                        # exit copy mode
Ctrlt+a,p       # put/paste the text in the desired location
```
### vim 与系统粘贴板互通
在命令行下输入命令：`vim --version | grep clipboard `
看一下输出结果中clipboard前面是+还是-，如果是+，这就意味着vim是可以与系统共享剪切板的<br/>
进入可视模式，`v`,选择需要选中的文字
在vim中，将文字放入系统粘贴板：<br/>
`" + y`
从系统粘贴板中提取文字到vim中：<br/>
`" + p`
### tmux problem
Using this works for me:
```
TMUX= tmux new-session -d -s name
tmux switch-client -t name
The TMUX= on the first line is required so tmux doesn't throw a sessions should be nested with care, unset $TMUX to force message.
```
### tmux2.8与系统粘贴板互通
参考：https://unix.stackexchange.com/questions/131011/use-system-clipboard-in-vi-copy-mode-in-tmux<br/>
https://blog.csdn.net/anribras/article/details/53965718<br/>
```
setw -g mode-keys         vi    # 进入复制模式的时候使用 vi 键位（默认是 EMACS）
unbind [
bind Escape copy-mode
unbind p
bind p paste-buffer
bind -Tcopy-mode-vi v send -X begin-selection
#bind -Tcopy-mode-vi y send -X copy-selection

bind -T copy-mode-vi y send-keys -X copy-pipe-and-cancel "xclip -i -f -selection primary | xclip -i -selection clipboard"
```
`c+a,escape`先进入可视模式,`v`选择文本，`y`将文本通过`xclip`输入到系统粘贴板
### tmux2.1与系统粘贴板互通
```
bind-key -t vi-copy y copy-pipe 'xclip -selection clipboard >/dev/null'
```
参考：https://unix.stackexchange.com/questions/131011/use-system-clipboard-in-vi-copy-mode-in-tmux<br/>
https://blog.csdn.net/anribras/article/details/53965718<br/>
整个配置文件如下：<br/>
```
#send prefix
set-option -g prefix C-b
#unbind-key C-b
bind-key C-b send-prefix

# Use Alt-arrow keys to switch panes
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

# Shift arrow to switch windows
bind -n S-Left previous-window
bind -n S-Right next-window

# Mouse mode
set -g mouse on
# Set easier window split keys
bind-key v split-window -h
bind-key h split-window -v

#vi
setw -g mode-keys vi
unbind [
bind Escape copy-mode
unbind p
bind p paste-buffer
bind-key -t vi-copy 'v' begin-selection
bind-key -t vi-copy y copy-pipe 'xclip -selection clipboard >/dev/null'
# Easy config reload
bind-key r source-file ~/.tmux.conf \; display-message "tmux.conf reloaded"
```
### shutdown over ssh
这是关机命令，在服务器上不要用，用`who`可以查看系统中用户的登录情况
You can try this command over SSH:

`sudo poweroff`
If you want to just send this command over SSH and authenticate in one go, append the command to the regular SSH command:

`ssh -t <options> <user>@<hostname> sudo poweroff`
### ssh remote login
https://www.digitalocean.com/community/tutorials/how-to-use-ssh-to-connect-to-a-remote-server-in-ubuntu#conclusion
`ssh remote_username@remote_host`<br/>
`ssh jucic@218.197.199.222`<br/>
`ssh qy@218.197.199.222`<br/>
可以使用图形：`ssh qy@218.197.199.222 -X`
### tmux查看版本号
` tmux -V`
### tmux常用命令
https://gist.github.com/ryerh/14b7c24dfd623ef8edc7
```
启动新会话：
tmux [new -s 会话名 -n 窗口名]
Detach 会话:
prefix+d
恢复会话：
tmux a [-t 会话名]
列出所有会话：
tmux ls
```
#### tmux会话
```
:new<回车>  启动新会话
s           列出所有会话
$           重命名当前会话
```
#### tmux调整窗口排序
```
swap-window -s 3 -t 1  交换 3 号和 1 号窗口
swap-window -t 1       交换当前和 1 号窗口
move-window -t 1       移动当前窗口到 1 号
```
#### 窗格（分割窗口）
```
%  垂直分割
"  水平分割
o  交换窗格
x  关闭窗格
⍽  左边这个符号代表空格键 - 切换布局
q 显示每个窗格是第几个，当数字出现的时候按数字几就选中第几个窗格
{ 与上一个窗格交换位置
} 与下一个窗格交换位置
z 切换窗格最大化/最小化
```
### conky 在桌面显示系统的cpu 内存等信息
http://blog.sina.com.cn/s/blog_69e5d8400102vr0x.html
http://www.junauza.com/2009/03/installset-up-conky-on-ubuntu.html

### 查看nvidia GPU的信息
`nvidia-smi`
### cuda 的版本
```
cat /usr/local/cuda/version.txt
```
### change the default shell
`chsh -s $(which zsh)`
### anaconda3 path of server
`export PATH=/home/qy/anaconda3/bin:$PATH`<br/>
`source activate gluon`
`source deactivate`

### 删除
```
# vim /etc/apt/sources.list
可以先将光标滚动到文件末尾使用命令
:1,.d
即删除从第一行到当前行，清空文件内容，然后 :wq 保存
"."当前行 ，"1,."表示从第一行到当前行 ，"d"删除
```
### 登入server 端口映射
```
ssh -L8008:localhost:8888 qy@218.197.199.222 -X
```
### Ubuntu 镜像使用帮助
https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/
### 清华大学开源软件镜像站
https://mirrors.tuna.tsinghua.edu.cn/
### logout ssh
```
法1：Ctrl+D
法2：输入 logout
```
### 终端打开文件管理器
```
在linux下开发时，使用最多的是终端，在某些情况下，想通过终端快速打开图形化的文件管理器，来管理当前目录，我们可以使用如下命令：
#nautilus . 
顺便说一下，在windos下使用 explorer .  
在mac os下使用 open  
```
### 前后台进程切换
https://blog.csdn.net/qq_36275734/article/details/82830669<br/>
`fg、bg、jobs、&、ctrl + z命令`
## screen 窗口管理器常用操作
https://blog.csdn.net/qq_36275734/article/details/82832722<br/>
https://www.tecmint.com/screen-commahaond-examples-to-manage-linux-terminals/<br/>
建立不同的会话：每建一个，然后detach ,然后再建，reattach(重新链接）输入会话的id比较好<br/>
```
创建会话：c+a -S [screen-name] 
-m 　即使目前已在会话中的screen会话，仍强制建立新的screen会话
查看所有会话：screen –ls
Reattach 会话：screen –r [screen-name]
Detach 会话: screen –d [screen name（id)]
ctrl + a + d：detach当前会话
ctrl + a + c：创建新窗口（create）
ctrl + a + w: 列出所有窗口
ctrl + a + A: 窗口重命名
ctrl + d：退出（关闭）当前窗口
```
### tmux ssh 远程连接时访问本地系统粘贴板的方法

https://medium.freecodecamp.org/tmux-in-practice-integration-with-system-clipboard-bcd72c62ff7b<br/>

https://hackernoon.com/tmux-in-practice-copy-text-from-remhttps://blog.csdn.net/YuZhiHui_No1/article/details/44564963ote-session-using-ssh-remote-tunnel-and-systemd-service-dd3c51bca1fa<br/>
其他的方法：
在.tmux.conf中关闭Mouse mode，就OK<br/>
#set -g mouse on<br/>
在命令终端，可以进行复制粘贴操作，有多个窗口时可以快捷键，`c+b+z`进行最大化，然后复制粘贴<br/>
编辑文件时，在vim中，也可以打开gedit图形界面（比较慢)，可以按`c+c``c+v`进行复制粘贴操作<br/>

### packages in environment at /home/qy/anaconda3:
` conda list --show-channel-urls`
### 列出anaconda中环境的路径
`conda info -e`
### anaconda创建环境、删除环境、激活环境、退出环境
```
Anaconda创建环境：
conda create -n [name] python=3.6 
删除环境（不要乱删啊啊啊）
conda remove -n [name] --all
激活环境
source activate [name]
退出环境
source deactivate
```
### 如何更改linux文件的拥有者及用户组(chown和chgrp)
https://blog.csdn.net/hudashi/article/details/7797393

### ananconda 安装nb_conda，解决jupyter notebook中环境的选择
https://my.oschina.net/flyrobin/blog/1546363
qy@BMEserver [08:42:05 AM] [~/anaconda3/bin] 
-> % ./conda install nb_conda
好像conda和pip是差不多的。
### cuda ImportError: libcublas.so.9.0: cannot open shared object file
https://blog.csdn.net/ksws0292756/article/details/80034086
### conda 前面不能用sudo ,可以直接找到conda命令的路径
在安装anaconda的时候，不要用sudo,否者安装的文件都是root的文件
```
sudo: conda: command not found
可以使用：
sudo path/to/conda install xxx
```
### github markdown(简书等）插入超链接和网络图片--github--markdown--
```
[要显示的文字](链接的地址)
[百度](https://www.baidu.com/)

叹号! + 方括号[ ] + 括号( )
在方括号里可以加入一些 标识性的信息
![](http://upload-images.jianshu.io/upload_images/1483901-4fc7e179642197ff.gif?imageMogr2/auto-orient/strip)
```
[百度](https://www.baidu.com/)<br/>
![百度](http://upload-images.jianshu.io/upload_images/1483901-4fc7e179642197ff.gif?imageMogr2/auto-orient/strip)<br/>

### Linux下监视NVIDIA的GPU使用情况--nvid--
https://blog.csdn.net/jasonzzj/article/details/52649174
```
$ nvidia-smi
```
```
监视显存：我们设置为每 1s 显示一次显存的情况：
$ watch -n 1 nvidia-smi
```
### vim替换--vim--
https://harttle.land/2016/08/08/vim-search-in-file.html
例如`:%s/foo/bar/g`会在全局范围(%)查找`foo`并替换为`bar`，所有出现都会被替换(g).
### git add files--git--github--
```
git add 文件夹/            添加整个文件夹及内容
git add *.文件类型       添加目录中所有此文件类型的文件 `*.文件类型`之后敲tab键，会显示挡墙目录下这个文件类型的所有文件
```
