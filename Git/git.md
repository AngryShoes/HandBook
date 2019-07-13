# Git guide

## 创建git账号之后的配置

    1. 首先要在本地创建一个ssh key 就是你现在需要在你电脑上获得一个秘钥
    ssh-keygen -t rsa -C "XXXXXXXXX@qq.com"引号内需要改成你在注册GitHub的时候绑定的邮箱账号创建的秘钥一般在 C:\Users\Administrator\.ssh 文件夹下

    2. 文本编辑器打开id_rsa.pub文件，把秘钥复制到github账户的SSH keys页面里点击添加,title 是让你给你的密匙起一个名字，根据个人喜好，什么名字都可以
       如下图所示。
    3. 输入ssh -T git@github.com来检查是否成功绑定。第一次绑定的时候输入上边的代码之后会提示是否continue，在输入yes后如果出现了：You've successfully authenticated, but GitHub does not provide shell access 。
    那就说明，已经成功连上了GitHub。接下来还需要简单的配置账户信息。
    4. git config --global user.name "your name"
     git config --global user.email "youremail@youremail.com"
     name最好和GitHub上边的一样，email是一定要是注册GitHub的那个邮箱地址

    5. 创建库 克隆库
      git clone git@github.com:AngryShoes/HandBook.git
      克隆仓库时有时会提示The authenticity of host 'github.com (xxx.xxx.xxx.xxx)' can't be established文件夹内少了一个known_hosts文件，本来密钥文件应该是三个，现在只有两个，便报了这样的错误，此时输入yes回车之后，生成了缺少了的known_hosts文件，便可解决这个问题

![add sshKey](https://github.com/AngryShoes/HandBook/blob/master/Git/images/addSSHKey.png)

![add authenticity](https://github.com/AngryShoes/HandBook/blob/master/Git/images/authenticity.png)

## 管理本地项目文件

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

    或者新建仓库同时添加README.md 和.gitignore,然后在本地git clone [repository name],添加要上传的文件

---

* 如果本地文件有修改再上传，由git status 查看哪些文件哪些内容变动，然后在git add [要上传的文件]

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

## 创建.gitignore文件

windows下创建.gitignore文件会提示“必须键入文件名”，所以可以考虑使用一下步骤：

    1. 创建文本文件命名为gitignore.txt       
    2. 打开文件，添加要过滤的规则然后保存并关闭文件       
    3. 按住Shift键在gitignore.txt所在文件夹右键“在此处打开命令窗口”  
    4. 在命令行中重命名：ren gitignore.txt .gitignore

为了避免出现上面的情况可以在要上传的同级目录下创建[.gitignore](http://blog.csdn.net/gjy211/article/details/51607347)文件

[Git使用详细教程](https://blog.csdn.net/youzhouliu/article/details/78952453)

[用法指南](http://www.cnblogs.com/specter45/p/github.html)

[删除文件](http://blog.csdn.net/wudinaniya/article/details/77508229)

[markdown文本编辑](http://blog.csdn.net/u011419965/article/details/50536937#1-强调)
