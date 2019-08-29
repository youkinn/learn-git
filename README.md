# learn-git

##### 配置提交作者
- git config user.name "youkinn2"
- git config user.email "03338277@163.com"

##### 代码拷贝
- git clone https://github.com/youkinn/learn-git.git
- 从远程拷贝代码

##### 查看变更日志
- git log
> git log 命令会产生版本库里乙烯利单独提交的历史.
> 使用 --oneline只显示一行的简洁信息.

##### 查看变更
- git status
> 查看当前暂存的更改(如果没有显示 "nothing to commit, working tree clean").

##### 查看暂存的文件
- git ls-files --stage/-s
 
##### 添加/取消暂存
- git add index.html
> 将index.html添加到版本库里边.

- git add .
> git log 把当前目录及其子目录的文件都添加到版本库里边.

- git rm --cached index.html
> 删除索引中的文件并把它保留在工作目录中. 与git reset HEAD filename区别?

- git rm index.html
> 将文件从索引和工作目录都删除. 删除前如果对文件有编辑过, 删除会失败. 可以添加-f参数强制删除.
> 不小心误删后, 可以使用 git checkout HEAD -- index.html 恢复.

###### 提交
- git commit -m "message"
> 提交暂存的更改

- git commit --all
> 提交已追踪的更改. 需要注意的是, 新追加的文件需要git add之后才会被提交.

- git commit
- 与 git commit -m "message"的区别是允许输入多提交消息, 默认进入vim的编辑界面.
- 第一行用于使用git log --oneline命令是显示.

###### vim
- i 切换到插入模式
- esc返回可视化模式
- :w 将文件写入磁盘并保存
- :q 退出编辑器, 回到命令行

##### 重命名
- git mv index.html index2.html
> 将index.html重命名为index2.html. 
> 重命名git log --follow index2.html 来查看历史记录

##### 放弃更改
- git checkout -- index.html
- 其实就是放弃更改.

##### 标签
- git tag init 0d7f482
> init是tag的名称, 可以是通常是某次上线或者其他重要节点. 
> fa04c30是一次提交的散列值的前7位
> tag其实就是散列值的别名，一旦设置了tag之后，就可以通过git tag命令查看所有的tag.
> 通过git show init 查看此次提交的内容(等同git show 0d7f482).


##### 分支
- git checkout -b test master
> 从master里边拉出一条叫做test的分支

- git branch -D test
> 删除名叫test的本地分支

- git checkout test
> 切换到本地test分支 origin/test为切换远程的test分支

- git branch -a
> 查看所有的分支(本地+远程) 列出的远程分支名字带remotes: remotes/origin/master

- git branch -r
- 查看所有远程分支 origin/master

- git fetch
> 远程分支列表不会自动更新, 使用fetch更新这个列表.
> 执行命令前, 你可能看不到其他人后来新增的远程分支.
