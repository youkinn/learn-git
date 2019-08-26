# learn-git

##### 配置提交作者
- git config user.name "youkinn2"
- git config user.email "03338277@163.com"

##### 查看变更日志
- git log
> git lot 命令会产生版本库里乙烯利单独提交的历史.

##### 查看暂存的变更
- git status
> 查看当前暂存的更改(如果没有显示 "nothing to commit, working tree clean").
 
##### 添加/取消暂存
- git add index.html
> 将index.html添加到版本库里边.

- git add .
> git log 把当前目录及其子目录的文件都添加到版本库里边.

- git reset HEAD index.html
> 取消暂存更改index.html

##### 删除/重命名
- git rm index.html
> 将index.html从版本库里边删除.

- git mv index.html index2.html
> 将index.html重命名为index2.html.

##### 放弃更改
- git checkout -- index.html
- 其实就是放弃更改(慎用).