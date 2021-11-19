## git学习

1. git初始化本地仓库

打开本地的文件夹仓库`git init`初始化本地仓库，若发现本地出现**隐藏文件夹**`.git`则初始化完成，可以进行之后的git操作。



2. git clone

一、直接复制远程库到本地库

从GitHub上克隆仓库，`git clone + github上的URL地址`

![image-20211119190810208](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20211119190810208.png)

成功后可以发现本地的仓库多了clone下来的文件

二、本地库直接链接到远程库

1.`git remote add origin + github上的URL地址` 

2.`git pull origin + main(分支名)`

以上两种方式都可以达到同样的效果



3. git add

修改本地仓库的项目文件后，采用`git add .`将项目文件从工作区(workspace)传到暂存区(Stage)



4. git push

使用`git add .`将仓库内所有的项目文件传到暂存区后，再次检查是否全部上传`git status`，若上传完毕，即可push到远程仓库(Remote)GitHub上。

`git push`完成后即可在GitHub上的仓库看到从本地推上去的所有项目文件。





### 让git和github关联起来

两者通过ssh连接，安全又快速

1. 查找公钥和密钥

打开C盘，我发现没找到`.ssh`文件。百度了一下，尝试使用cmd命令行`ssh-keygen -t rsa -C"xxxxx@xxxxx.com`找到file位置，但是还是没找到`.ssh`文件。

搜索后发现的解决方法。自己生成新的SSH密钥

打开**git bash**

`git config --global user.name"XXX"`(输入用户名)

`git config --global user.email"XXX@XXX.com"`(输入邮箱)

`ssh-keygen -t rsa-C"your_email@example.com"`

然后会提示**Enter file  in which to save the key**后面是一个路径，就能找到想要的`.ssh`文件夹。

2. 设置GitHub上的密钥

将本地文件中`.ssh`文件的id_rsa.pub内的内容，复制到GitHub账户setting的ssh中即可。

3. 测试ssh key是否成功

使用命令`ssh -T git@github.com`，如果出现`You've successfully authenticated,but Github does not provide shell access`这就表示已成功连上GitHub。



### git报错

1. `your branch is up to date with 'origin/main'`报错

报错背景：git切换分支`git checkout main`时出现报错`your branch is up to date with 'origin/main'`

​						检查文件`git status`时出现报错`your branch is up to date with 'origin/main'`

​						执行`git commit `时出现报错`your branch is up to date with 'origin/main'`

报错原因：你需要提交的文件和你当前的远程仓库origin下的main分支中的已存在的文件一模一样，所以没必要重新提交一次，因此会发出这样的提示。可以git diff一下，看有没有输出内容，如果没有就说明你要提交的文件和远程的一样，可以如此进行验证。

解决方法： 因此该问题没必要解决，事实上是你重复提交。



2. `Branch 'main' set up to track remote branch 'main' from 'origin'`报错

报错背景：![image-20211119202443436](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20211119202443436.png)

报错原因：根本原因在于推送的分支没有做commit操作

解决方法：![image-20211119202704905](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20211119202704905.png)

即可push成功![image-20211119202828605](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20211119202828605.png)