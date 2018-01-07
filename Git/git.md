## Git guide
---
    git init //把这个目录变成Git可以管理的仓库
    git add README.md //文件添加到仓库
    git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了 
    git commit -m "first commit" //把文件提交到仓库
    git remote add origin git@github.com:wangjiax9/practice.git //关联远程仓库  
    git push -u origin master //把本地库的所有内容推送到远程库上
 
  For example:
    
    1.git init

    2.git add README.md

    3.git commit -m "first commit"

    4.git remote add origin git@github.com:AngryShoes/HandBook.git

    5.git push -u origin master

---
上面的步骤是上传文件的基本步骤，刚开始上传时会把不必要的文件上传过去而github又没有删除文件夹的选项
所以只能在git客户端上删除然后再提交上去：
首先进入你的master文件夹下, Git Bash Here ,打开命令窗口

* $ git --help 帮助命令
* $ git pull origin master 将远程仓库里面的项目拉下来
* $ dir  查看有哪些文件夹
* $ git rm -r --cached target  删除target文件夹
* $ git commit -m '删除了target'  提交,添加操作说明
* $ git push -u origin master 最后再将本次更改更新到github项目上去

为了避免出现上面的情况可以在要上传的同级目录下创建[.gitignore](http://blog.csdn.net/gjy211/article/details/51607347)文件
上面的笔记部分参考了下面三位大牛的博客，如果有冒犯您请及时联系我会及时处理。

[用法指南](http://www.cnblogs.com/specter45/p/github.html)

[删除文件](http://blog.csdn.net/wudinaniya/article/details/77508229)

[markdown文本编辑](http://blog.csdn.net/u011419965/article/details/50536937#1-强调)