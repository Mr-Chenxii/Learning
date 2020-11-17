---

---

# 初识github 2020.11.05

 ## 1、拥有自己的第一个github账户

上C语言课的时候用手机创的。。过程方便快捷，QQ邮箱也可以注册，进去的时候全英文的网站给我一脸懵逼。。

[我的github](https://github.com/Mr-Chenxii)

下面上图!

![我的照片](C:\Users\windows\Desktop\新建文件夹\GitHub2.png)

## 2、电脑上下载Git

* 1、刚开始跑到官网去下载，这下载速率真的惊到我了。。
* 2、后面到菜鸟教程上搜索Git教程才发现有镜像包可以下载。

[Git下载链接](https://npm.taobao.org/mirrors/git-for-windows/)

* 3、安装成功

  ![我的照片](C:\Users\windows\Desktop\新建文件夹\Git.png)

## 3、学习Git的一些基本操作

学了之后才发现Git上就可以访问Github的仓库，根本不需要用到浏览器。。逐渐脱离图形化，有点`hacker`的感觉了。哈哈哈

基本原理，文件先从工作区添加(add)到缓存区（stage)，再提交到(commit)主分支内。



### 3.1查看仓库状态

```java
执行 git init创建一个新的仓库
    git status查看仓库状态
  git cmd上显示  On branch main
            No commits yet
```

### 3.2暂存文件与提交文件

```java
首先在仓库内新建一个文件
    查看仓库状态后
    会提示 (use "git add <file>..."to include in what will be committed)
    nothing added to commit but untracked files present (use "git add" to track)
    执行 git add .
    再次执行 git status
    会发现 上面的提示已经消失
    出现新提示（use "git rm --cached<file>..." to unstage) new file:
    
    执行git commit -m(加注释)
        此时文件已经成功提交到主分支内
        再次查看仓库状态git status
        可知工作区没有新的文件可以添加
```

### 3.3将文件提交到github上。

1. 首先关联你的github账户

```c
在git cmd上输入 git remote add (你的github地址)
    成功后可以使用 git remote -v查看状态
    使用 git push上传你的仓库文件
    
```





