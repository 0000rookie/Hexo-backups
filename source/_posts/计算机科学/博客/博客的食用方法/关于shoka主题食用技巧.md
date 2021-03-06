---
title: 关于shoka主题食用技巧
tags:
  - 博客
  - 教程
categories:
  - 计算机科学
  - 博客
  - 博客的食用方法
path: 计算机科学\博客\博客的食用方法
abbrlink: 5d5981b0
date: 2022-04-03 01:36:30
---

## 首页置顶文章

```markdown mark:2-3
---
title: 置顶文章
sticky: true
---
```

## 关闭文章评论

```markdown mark:2-3
---
title: 开启文章评论
comment: false
---
```

## 关闭文章音乐播放器

```markdown mark:2-3
---
title: 关闭文章音乐播放器
audio: false
---
```

## 个人头像配置

```yaml mark:1-7
sidebar:
  # 侧边栏的位置
  position: left
  #position: right
  # 替换默认头像，并在这里设置url
  avatar: avatar.jpg
  # 头像路径在 themes\shoka\source\images\avatar.jpg
```

## 底部widgets

```yaml mark:1-4
widgets:
  random_posts: true # 显示随机文章
  recent_comments: true # 显示最近评论
  #在shoka/_config.yml修改
```

## `note`提示块

``` mark:1,2-28
:::default
默认默认
:::

:::primary
基本基本
:::

:::info
提示提示
:::

:::success
成功成功
:::

:::warning
警告警告
:::

:::danger
危险危险
:::

:::danger no-icon
危险危险
:::
```

:::default
默认默认
:::

:::primary
基本基本
:::

:::info
提示提示
:::

:::success
成功成功
:::

:::warning
警告警告
:::

:::danger
危险危险
:::

:::danger no-icon
危险危险
:::

## collapse折叠块

能基于 `markdown-it-container`
标签为：
开始行	`+++[风格颜色] [标题文字]`
结束行	`+++`

```mark:1,2-42
+++ 默认默认 这里是一段文字
++ 下划线 ++
+++


+++primary 紫色
:::info
参考信息
:::

- 第一行
- 第二行
+++


+++info  蓝色
;;;id3 卡片 1
这里是卡片 1 的内容
;;;

;;;id3 卡片 2
这里是卡片 2 的内容
;;;
+++

+++success 绿色
{% links %}
- site: 優萌初華
  url: https://shoka.lostyu.me
  color: "#e9546b"
{% endlinks %}
+++

+++warning 黄色
!! 警告警告警告警告警告！！{.bulr}
[label]{.label .success}
+++

+++danger 红色
[danger]{.label .danger}
+++
```

+++ 默认默认 这里是一段文字
++ 下划线 ++

+++


+++primary 紫色
:::info
参考信息
:::

- 第一行
- 第二行
+++


+++info  蓝色
;;;id3 卡片 1
这里是卡片 1 的内容
;;;

;;;id3 卡片 2
这里是卡片 2 的内容
;;;
+++

+++success 绿色
{% links %}
- site: 優萌初華
  url: https://shoka.lostyu.me
  color: "#e9546b"
  {% endlinks %}
+++

+++warning 黄色
!! 警告警告警告警告警告！！{.bulr}
[label]{.label .success}
+++

+++danger 红色
[danger]{.label .danger}

+++
