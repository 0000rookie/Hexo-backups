---
title: 第三篇：Git提交文件---从0基础搭建Hexo博客
tags:
  - 博客
  - 教程
categories:
  - 计算机科学
  - 博客
  - 零基础搭建Hexo个人博客系列
path: 计算机科学\博客\零基础搭建Hexo个人博客系列
abbrlink: b75a1db6
date: 2022-03-30 00:22:45
updated: 
---

## 配置git

#### 一、绑定Gitee

首先来简单介绍一下SSH协议

**SSH（安全外壳协议，Secure Shell 的缩写）是建立在应用层基础上的安全协议。SSH 是目前较可靠，专为远程登录会话和其他网络服务提供安全性的协议，利用 SSH 协议可以有效防止远程管理过程中的信息泄露问题。简单来说，SSH就是保障你的账户安全，将你的数据加密压缩，不仅防止其他人截获你的数据，还能加快传输速度。如果想详细了解的话，可以看这篇文章：详述 SSH 的原理及其应用 - CSDN，下面就详细介绍如何绑定GitHub和提交文件。**



**我们要用git上传文件到GitHub首先得利用SSH登录远程主机，而登录方式有两种：一种是口令登录；另一种是公钥登录。口令登录每次都要输入密码十分麻烦，而公钥登录就省去了输入密码的步骤，所以我们选择公钥授权。首先我们得在 GitHub 上添加 SSH key 配置，要想生成SSH key，就要先安装 SSH，不过我们安装了 Git Bash，其应该自带了 SSH。检验一下是否安装 SSH，我们在新建的文件夹中右键打开 Git Bash：**

1. 新建一个文件夹``text`

   ![](https://s2.loli.net/2022/03/30/Jz1dTG6SPkwlQ5p.jpg)

2. 鼠标右击打开`git Bash Here`

   ![](https://s2.loli.net/2022/03/30/Jz1dTG6SPkwlQ5p.jpg)

3. 输入`ssh`检查使是否安装`ssh`

   ```bash mark:1
   ssh-keygen -t rsa
   ```

   

![](https://s2.loli.net/2022/03/30/8RcNpfrZ2PEjtA7.jpg)

4. 输入 `ssh-keygen -t rsa`命令，表示`RSA`算法生成密钥，然后敲4次回车键，之后会生成两个文件，分别为密钥`id_rsa`和公钥`id_rsa.pub`

   ```bash mark:1
   ssh-keygen -t rsa
   ```
   
   

![](https://s2.loli.net/2022/03/30/K3mfVxdr54IvaLJ.jpg)

![](https://s2.loli.net/2022/03/30/9fNDbOAVUBeWd8G.jpg)



**接下来我们要做的事情就是把公钥` id_rsa.pub `的内容添加到` GitHub`。复制公钥 `id_rsa.pub` 文件里的内容，你可以通过目录找到 `id_rsa.pub` 文件的位置，用记事本打开文件复制。**

5. 打开 `id_rsa.pub`文件复制

![](https://s2.loli.net/2022/03/30/s39ZxPGuTDJLmwF.jpg)



6. 打开`github--->settings--->SSH and GPG keys--->New SSH key`

![](https://s2.loli.net/2022/03/30/LhUzwCNnZGOXDl9.jpg)



![](https://s2.loli.net/2022/03/30/4vtGl98ehjRWKJd.jpg)

**粘贴内容进去**

![](https://s2.loli.net/2022/03/30/i1b3hoFvzPWcUje.jpg)

**添加成功**

![](https://s2.loli.net/2022/03/30/h7npjw9I8qOBaXA.jpg)



**验证是否成功，在`Git Bash`中输入` ssh -T git@github.com`验证**

```bash mark:1
ssh -T git@github.com
```



首次需要输入```yes```

![](https://s2.loli.net/2022/03/30/EHSFLzxKoIavPcr.jpg)



#### 二、接下来是提交文件

1. 新建仓库

![](https://s2.loli.net/2022/03/30/VKYp3k8NMgDvrW1.jpg)

2. 给仓库起个名

![](https://s2.loli.net/2022/03/30/zsE5a7B3KrliXny.jpg)

3. 复制仓库`HTTPS`链接

![](https://s2.loli.net/2022/03/30/YVpZtKBoWgPbzme.jpg)

4. 将`text`仓库`clone`到本地仓库，返回刚刚`Git`的窗口，输入`git clone 链接`。

   ```bash mark:1
   git clone https://github.com/aliang518/text.git
   ```
   
   

![](https://s2.loli.net/2022/03/30/6KVx9MoJ48mE25k.jpg)

5. 打开刚刚在电脑新建的`text`文件夹是不是存在一个`GitHub`上名为的`text`仓库

![](https://s2.loli.net/2022/03/30/b7dHYj5e3lCxypg.jpg)

6. 查看`text`仓库是不是和`GitHub`的仓库内容一样

![](https://s2.loli.net/2022/03/30/g6nQxiVeCzubkNj.jpg)

7. 新建一个文件

   ![](https://s2.loli.net/2022/03/30/2emTn6GyiqSZIba.jpg)

8. 在此文件夹下进入`Git Bash Here`

![](https://s2.loli.net/2022/03/30/7bi2eu8FNYTltd1.jpg)

9. 输入`git status`命令查看仓库状态

   ```bash mark:1
   git status
   ```
   
   

![20](http://cdn.jsdelivr.net/gh/0000rookie/imgs/Hexoimgs/pmlipmng202204011752.jpg)

10. `hexo` 已经是一个 Git 仓库了，而我们刚刚创建的文件`123.txt` 没有被追踪，也就是没有提交到本地仓库。现在我们使用 `git add `命令将文件添加到了「临时缓冲区」，再用 `git commit -m "`提交信息" 将其提交到本地仓库，如下图

    ```bash
    git add text.txt
    git commit -m "提交信息"
    ```

![](https://s2.loli.net/2022/03/30/cK8LmrBq3vh9YQo.jpg)

![](https://s2.loli.net/2022/03/30/3ltIPmEFkHKU1Bc.jpg)

如果你是第一次提交的话，就会出现下图情况，让你输入账号和邮箱

```bash
```git config --global user.name "aliang518"
git config --global user.email "aa******56@126.com"
```

![](https://s2.loli.net/2022/03/30/Dbag4oklMAp1XqQ.jpg)





11. 查看仓库提交日志

    ```bash mark:1
    git log

![](https://s2.loli.net/2022/03/30/xCkvay35W4zG8gE.jpg)



12. 再输入 `git status` 查看一下仓库状态

    ```bash mark:1
    git status
    ```
    
    

![](https://s2.loli.net/2022/03/30/DKZzdOLexy1lB52.jpg)

13. 将本地仓库提交到远程仓库

    ```bash mark:1
    git push origin main
    ```

    

![](https://s2.loli.net/2022/03/30/rFebnLUxqSkCoR3.jpg)

14. 从浏览器打开的时候选择你已经登录`GitHub`的那个浏览器(我这里用火狐浏览器)

![](https://s2.loli.net/2022/03/30/etGBbrAjaOzH9Qk.jpg)

15. 等待上次成功

![](https://s2.loli.net/2022/03/30/16UjrZte4OydkG8.jpg)

16.  打开`GitHub`仓库`F5`刷新一下，会出现刚刚在本地`text`目录新建的`text.txt`文件

![](https://s2.loli.net/2022/03/30/QvD1LZXAqeWSNJf.jpg)

**提交文件已经成功啦**
