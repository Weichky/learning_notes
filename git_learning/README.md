<center><b>注意：单引号用于代称。如 'branch' 指某分支</b></center>

查看仓库状态
`git status`

初始化Git仓库
`git init`

将文件添加到Git仓库
`git add`*可以加`.`来表示整个文件夹内所有文件*

记录包括当前暂存区内容和给定日志的新提交
`git commit -m 'message'` 

创建分支
`git branch 'branch'`

`-d`符号删除branch

切入分支
`git checkout 'branch'`

合并branch
`git merge 'branch'`*合并入当前指向的'branch'*

添加标签
`git tag 'tag'`

添加远程仓库
`git remote add '仓库名' 'url'`

同步远程仓库
`git pull 'repository' 'branch'`*下行*
`git push 'repository' 'branch'`*上行*

显示commit历史
`git log`

修改刚刚的commit
`git commit --amend`

强制版本覆盖
`git fetch --all`
`git reset --hard main`

设置代理
`git config --global http.proxy 127.0.0.1:xxxx`
`git config --global https.proxy 127.0.0.1:xxxx`

查看代理
参数`--get`

取消代理
参数`--unset`

设置`config`
`--list`
`user.name`
`user.email`