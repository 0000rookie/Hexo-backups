---
title: 第六篇：将博客部署到GitHub---从0基础搭建Hexo博客
tags:
  - 博客
  - 教程
categories:
  - 计算机科学
  - 博客
  - 零基础搭建Hexo个人博客系列
path: 计算机科学\博客\零基础搭建Hexo个人博客系列
abbrlink: dc09a46c

date: 2022-03-30 00:25:37
updated: 
---



## 将Hexo部署到github

1. 打开`blog`文件夹，打开`_config.yml`文件

![](https://s2.loli.net/2022/03/30/XsNufKGeyItOwnB.jpg)

2. 滑到最下面找到如图

![](https://s2.loli.net/2022/03/30/heHXcG2u1anBOAI.jpg)

3. `打开仓库--->code--->SSH--->copy`，复制`SSH`的链接

   ![](https://s2.loli.net/2022/03/30/ewWNlivjaSzXo2f.jpg)

4. 填到`步骤2 `的文件中。如下图


![](http://cdn.jsdelivr.net/gh/0000rookie/imgs/Hexoimgs/pmlipmng202204012026.jpg)

```yml
deploy:
  type: git
  repo: git@github.com:0000rookie/github.io.git
  branch: main
```

5. 回到`blog`文件夹中，鼠标右键打开`git bash here`，安装`git`部署插件

   ```bash mark:1
   npm install hexo-deployer-git --save
   ```

![](https://s2.loli.net/2022/03/30/3bDkNml7QBJVR6C.jpg)

6. 依次输入以下三条命令，

   ```bash mark:1,2-3
   hexo clean 
   hexo g
   hexo d
   ```

![](https://s2.loli.net/2022/03/30/gucNPIbDdVnfw9v.jpg)

![](https://s2.loli.net/2022/03/30/ROfaZgmzFwec1ND.jpg)

7. 这是浏览器打开`https://aliang518.github.io/`就是你的博客了

   ```html mark:1
   https://aliang518.github.io/
   ```


![](https://s2.loli.net/2022/03/30/VeGUNhMdplYP5rz.jpg)





























