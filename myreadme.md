# record some information

## git

### git commit操作以及退出日志编辑状态

https://blog.csdn.net/huakaiba/category_2490439.html)

刚进去时发现怎么也输入都没反应，是因为此时vim编辑器处于不可编辑状态，输入字母 `c` 可以进入编辑状态，这个时候就可以修改注释信息啦 ~

修改完之后按`esc`键退出编辑状态，再按大写`ZZ`就可以保存退出vim编辑器。

### git checkout

命令`git checkout -- readme.txt`意思就是，把`readme.txt`文件在工作区的修改全部撤销，这里有两种情况：

一种是`readme.txt`自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是`readme.txt`已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

总之，就是让这个文件回到最近一次`git commit`或`git add`时的状态。

现在，看看`readme.txt`的文件内容：

```
$ cat readme.txt
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
```

文件内容果然复原了。

`git checkout -- file`命令中的`--`很重要，没有`--`，就变成了“切换到另一个分支”的命令，我们在后面的分支管理中会再次遇到`git checkout`命令。



(use "git restore --staged <file>..." to unstage)

### ssh

查看 ssh 公钥方法：

1.通过命令窗口
a. 打开你的 git bash 窗口
b. 进入 .ssh 目录：cd ~/.ssh
c. 找到 id_rsa.pub 文件：ls
d. 查看公钥：cat id_rsa.pub 或者 vim id_rsa.pub



[添加远程库 - 廖雪峰的官方网站 (liaoxuefeng.com)](https://www.liaoxuefeng.com/wiki/896043488029600/898732864121440)

[从远程库克隆 - 廖雪峰的官方网站 (liaoxuefeng.com)](https://www.liaoxuefeng.com/wiki/896043488029600/898732792973664)

### 退出正在运行的git指令

q

### 提交到远程仓库

git push origin master

### 分支

>  创建并切换到dev分支（-c表示创建）
>
> $ git switch -c dev

> git branch 查看当前分支

> dev分支的工作完成，就可以切换回master分支
>
> $ git switch master

> 处于master分支的时候，合并dev的工作成果到master
>
> $ git merge dev

> 合并完成后，删除dev分支
>
> $ git branch -d dev

> **注意：git checkout -- <file>是撤销修改**

