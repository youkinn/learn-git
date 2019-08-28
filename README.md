# learn-git

##### 配置提交作者
- git config user.name "youkinn2"
- git config user.email "03338277@163.com"

##### 代码拷贝
- git clone https://github.com/youkinn/learn-git.git
- 从远程拷贝代码

##### 查看变更日志
- git log
> git lot 命令会产生版本库里乙烯利单独提交的历史.

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
> 删除索引中的文件并把它保留在工作目录中.

- git rm index.html
> 将文件从索引和工作目录都删除. 删除前如果对文件有编辑过, 删除会失败. 可以添加-f参数强制删除.
> 不小心误删后, 可以使用 git checkout HEAD -- index.html 恢复.

###### 提交
- git commit
> 提交暂存的更改

- git commit --all
> 提交已追踪的更改. 需要注意的是, 新追加的文件需要git add之后才会被提交.

##### 重命名
- git mv index.html index2.html
> 将index.html重命名为index2.html. 疑问: 重命名后如何用git log查看历史记录

##### 放弃更改
- git checkout -- index.html
- 其实就是放弃更改.