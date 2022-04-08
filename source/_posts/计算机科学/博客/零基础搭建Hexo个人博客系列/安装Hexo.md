---
title: 第五篇：安装Hexo---从0基础搭建Hexo博客
tags:
  - 博客
  - 教程
categories:
  - 计算机科学
  - 博客
  - 零基础搭建Hexo个人博客系列
path: 计算机科学\博客\零基础搭建Hexo个人博客系列
abbrlink: 87b69652

date: 2022-03-30 00:25:26
updated: 
---

### 安装Hexo

1. 新建一个仓库

![](https://s2.loli.net/2022/03/30/LoeECmrFSydhnIt.jpg)

2. 给仓库起个名，格式为  `账号名.github.io`

![](https://tva4.sinaimg.cn/large/0065wfS6ly8h0rslvrth9j31ha0pqq5w.jpg)

3. 打开`stetings`

![](https://s2.loli.net/2022/03/30/KaQX5eUTYvWp9H6.jpg)

4. 滑到下面，找到这个`GitHub pages` ，点击打开

![](https://tva3.sinaimg.cn/large/0065wfS6ly8h0rsme8aiaj30p905tmx8.jpg)

5. 出现以下图说明成功了

![05](http://cdn.jsdelivr.net/gh/0000rookie/imgs/Hexoimgs/05.jpg)

6. 新建一个`blog`文件夹，在`blog`文件夹打开`git bash here`

![](https://s2.loli.net/2022/03/30/w8UDo5gxLzbOtiu.jpg)7. 安装`hexo-cli`插件

``` bash mark:1
npm install -g hexo-cli
```

![](https://s2.loli.net/2022/03/30/IHBmwDz6FaGUyVW.jpg)



8. 初始化博客

```bash mark:1
hexo init
```

![](https://s2.loli.net/2022/03/30/X4pArW28NVYmuCa.jpg)

9. 静态部署博客

```bash mark：1
hexo g
```

![09](https://tva1.sinaimg.cn/large/0065wfS6ly8h0rsqg2bmbj30l20gdtav.jpg)

10. 打开本地服务器

    ```bash mark:1
    hexo s
    ```

![](https://s2.loli.net/2022/03/30/atwxZphQzjf2kTi.jpg)

11. 浏览器输入`localhost:4000`查看

    ```bash
    localhost:4000
    ```

![10](https://tva2.sinaimg.cn/large/0065wfS6ly8h0rsqxer30j31ha0opdiy.jpg)

12. `ctrl+s`，停止本地服务器运行

**目前博客已经基本完成了**
