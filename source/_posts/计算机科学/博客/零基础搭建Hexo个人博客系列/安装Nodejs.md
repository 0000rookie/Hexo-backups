---
title: 第四篇：安装Nodejs---从0基础搭建Hexo博客
tags:
  - 博客
  - 教程
categories:
  - 计算机科学
  - 博客
  - 零基础搭建Hexo个人博客系列
path: 计算机科学\博客\零基础搭建Hexo个人博客系列
abbrlink: cf63c07
date: 2022-03-30 00:24:41
updated: 
---

## Node.js安装及配置环境

### `node.js`安装

1. 我这里安装在`C:\app\nodejs`

![](https://s2.loli.net/2022/03/30/N2pSe6Oq9BVLjbK.png)

2. 安装完之后打开`cmd`，输入`node -v`和`npm -v`

![](https://s2.loli.net/2022/03/30/Cln8IqXUAWwdMBK.jpg)



### 设置npm在安装全局模块时的路径和环境变量

如果不设置的话，安装模块是默认在C盘的，会占用C盘空间，我这边把安装路径修改一下，建议你也改一下。

1. 在`nodejs`下创建两个目录`ndoe_cache`和`node_global`

   ![](https://s2.loli.net/2022/03/30/il5vILhOF76qTRs.png)

2. 选择`node_cache`右击打开属性，把权限下的“完全控制”选上

![](https://s2.loli.net/2022/03/30/o8THeYdwjvLzSmb.png)

3. 同理，选择`node_global`右击打开属性，把权限下的“完全控制”也选上

![](https://s2.loli.net/2022/03/30/iETUhyYIKm7q9FL.jpg)



4. 复制`node_global`和`node_cache`的路径

![](https://s2.loli.net/2022/03/30/Aw8O2gfGHMUWeku.jpg)

5. 然后再返回刚刚打开的cmd,输入以下代码

```bash mark:1,2
npm config set prefix "C:\app\nodejs\node_global"
npm config set cache "C:\app\nodejs\node_cache"
```







![](https://s2.loli.net/2022/03/30/piUmIH6Zv9SO8c3.jpg)



6. 设置完路径之后,我们还要去系统环境变量修改一下

   **打开桌面--->此电脑--->属性--->高级系统设置--->环境变量**

![](https://s2.loli.net/2022/03/30/FyrUTcpvfkuGBAP.jpg)

7. 打开高级系统设置

![](https://s2.loli.net/2022/03/30/QvpAOLeS53EbMj9.jpg)

8. 打开环境变量

![](https://s2.loli.net/2022/03/30/xVQKP2vjLJ83ztU.jpg)

9. 在系统变量中新建一个变量,名为`NODE_PATH`,值为`C:\app\nodejs\node_global\node_modules`

![](https://s2.loli.net/2022/03/30/53jV6FgzIcTXSM8.jpg)

![](https://s2.loli.net/2022/03/30/Ust62PMjuSJ9iWw.jpg)



10.  然后编辑上方的用户变量的Path,编辑修改为`C:\app\nodejs\node_global`

![](https://s2.loli.net/2022/03/30/btcT8qOj6dkENLX.jpg)

![](https://s2.loli.net/2022/03/30/dnw9lCxOqj1GAH2.jpg)

![](https://s2.loli.net/2022/03/30/nYmStTyWgz4bejo.jpg)



### 全部变量修改结果,如下图

![](https://s2.loli.net/2022/03/30/HUSnKtdhMBgvcOq.jpg)



1. 然后打开`cmd`测试一下路径设置和环境变量有没有设置正确,如果没有设置正确的话,在`node_global`是看不到有`webpack`文件夹的

**安装过程**

![](https://s2.loli.net/2022/03/30/FY1g5nJesScwHvC.jpg)

**安装成功**

![](https://s2.loli.net/2022/03/30/8H7v1uoA3zn9WKs.jpg)

2. 出现以下路径说明安装成功了`node_global--->node_modules--->webpack`

![](https://s2.loli.net/2022/03/30/ugOVX3WGfpZ9DqP.jpg)



**`nodejs`环境配置到此就完成啦**

