git常用命令
创建README.md: echo “# notebook” >> README.md 
将一个文件夹初始化为一个git仓库：$ git init
```
跟踪文件：$ git add xxx
显示当前git的状态：$ git status
将跟踪后的文件提交：$ git commit -m ‘xxxx’
推送到远程仓库：git push -u origin master
```
```
查看已提交后的文件：git log –pretty=format:”” –name-only -1　

或者　git log –oneline –name-only -1 
或者　git log –stat　（列出所有的提交历史的记录，显示文件名）

# –name-only 只显示文件名 
git log –name-only -1 
# –pretty=format:”” 格式化commit message 这里什么都不显示 
git log –pretty=format:”” -1 
# 最终 
git log –pretty=format:”” –name-only -1 
```
github仓库：https://github.com/qyzhizi/programme_python.git
使用http方式添加远程仓库：git remote add origin https://github.com/qyzhizi/programme_python.git 
更换并使用ssh的链接方式：git remote rm origin
git remote add origin git@github.com:账户名/项目名.git　　　


撤销操作的语法：
git checkout – 文件名　链接：https://blog.csdn.net/qq_28602957/article/details/70194216

```
从github合并到本地文件：$ git pull origin master
```
### 查看远程仓库的地址
```
git remote -v
```
用户名更改：Qing-Yu-1 -> qyzhizi

```
echo "# notebook" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/qyzhizi/notebook.git
git push -u origin master

…or push an existing repository from the command line
git remote add origin https://github.com/qyzhizi/notebook.git
git push -u origin master
```
my common profile
git@github.com:Qing-Yu-1/notebook.git