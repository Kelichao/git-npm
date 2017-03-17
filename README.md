# git

- [传文件到github](http://www.jianshu.com/p/08656eb84974)

- [git图文教程](http://blog.sina.com.cn/s/blog_157ba6f0e0102wvmv.html)

- [git图文教程2](http://www.cnblogs.com/tugenhua0707/p/4050072.html)


# 命令行常用命令

- mkdir learngit# 创建learngit文件夹
- cd learngit# 从版本库文件夹进入到learngit文件夹
- pwd# pwd命令用于显示当前目录
- rm aaa.txt# 删除目录中的文件

# 普通git命令

>  配置全局git

- git config --global user.name "Kelichao" # 设置名字
- git config --global user.email "961904564@qq.com"# 设置git邮箱
- git config --global user.name #  取得名字->Kelichao
- git init # 把当前文件夹做成git仓库,生成隐藏.git文件

> git文件操作

- git add readme.txt     #将文件添加到缓存区，用于提交
- git commit -m "我提交了一个文件"   #正式提交,–m 后面的是注释
- git status # 查看提交状态(缓存区状态)
- git diff  XX      查看XX文件修改了那些内容
- cat readme.txt # 显示文件的内容 
- git log   #显示日志列表
- git git log --pretty=oneline #显示简洁版的日志
- git rm XX          删除XX文件

> 回退操作

- git reset  --hard HEAD^ #回退到前一次
- git reset  --hard HEAD^^ #回退到前两次
- git reset  –hard HEAD~100 #如果次数多的话，会退到前100次
- git reflog #恢复命令的查看列表,查看历史记录的版本号id
- git reset --hard 86b2399 #把代码恢复到了该版本
- git checkout  --  readme.txt #撤销文件在工作区的修改全部撤销。

> 与github代码库之间的联系

- git clone git@github.com:Kelichao/gittest.git# 克隆该站点的代码到本地
- git clone -b testmdev git@github.com:Kelichao/gittest.git# 克隆分支testmdev代码到本地
- git remote rm origin #删除之前的远程Git仓库连接
- git remote add origin git@github.com:Kelichao/gittest.git# 链接到对应代码库
- git push –u(第一次要用-u 以后不需要) origin master # 把当前master分支推送到远程库
- git push origin master#  把当前master分支推送到远程库

> 分支操作

-  git checkout –b dev  创建dev分支 并切换到dev分支上
-   git branch  查看当前所有的分支
-   git checkout master 切换回master分支
-  git merge dev    在当前的分支上合并dev分支
-   git branch –d dev 删除dev分支
-  git branch name  创建分支
-  git stash 把当前的工作隐藏起来 等以后恢复现场后继续工作
-  git stash list 查看所有被隐藏的文件列表
-  git stash apply 恢复被隐藏的文件，但是内容不删除
-   git stash drop 删除文件
-   git stash pop 恢复文件的同时 也删除文件
-   git remote 查看远程库的信息
-   git remote –v 查看远程库的详细信息
-   git push origin master  Git会把master分支推送到远程库对应的远程分支上
