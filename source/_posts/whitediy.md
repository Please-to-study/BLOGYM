---
title: 'White主题主页title改为今日诗词' 
date: 2020-7-28 13:19:36
tags: [随笔] 
cover: https://cdn.jsdelivr.net/gh/tangxuchao/tuku/%E7%81%B5%E9%AD%82%E8%8E%B2%E5%8D%8E-%E5%85%A8.jpg
---
主题源库：[点击进入](https://github.com/FuShaoLei/hexo-theme-white)

DIY前提：自己已经搭建完成。

## 一、修改title：

将主题_config.yml中：

```
# 自我介绍
intro:
  title: Hi.I'm White.
```

改为：

```
# 自我介绍
intro:
  title: '<p id="jinrishici-sentence">获取中...</p>
<script src="https://sdk.jinrishici.com/v2/browser/jinrishici.js" charset="utf-8"></script>'
```

## 二、修改引用

位置：themes/white/layout/_partial/mode-home.ejs

将：

```
<div class="intro-title animate__animated  animate__fadeInUp"><%=theme.intro.title%></div>
<div class="intro-sub animate__animated  animate__fadeInUp"><%- markdown(theme.intro.sub) %></div>
```

改为：

```
<div class="intro-title animate__animated  animate__fadeInUp"><%- markdown(theme.intro.title) %></div>
<div class="intro-sub animate__animated  animate__fadeInUp"><%- markdown(theme.intro.sub) %></div>
```

## 三：美化title（可选）

因为有些诗词句子太长会变成两行。

有两个修改办法：

### 1、修改主题宽度。

将主题_config.yml中：

```
style:
  layout:
    max-width: "1125px" #最大宽度
```

按你自己想法修改（可能影响美观）。

### 2、修改title字体大小

位置：themes/white/source/css/_page/layout.styl中：

```
.intro-title 
  font-family Gothic
  font-size 3em #修改此处即为字体大小
  font-weight 1000
  margin 0
  padding 0
```

### 3、修改主题布局

位置：themes/white/source/css/_page/layout.styl

```
/* home */
.intro-content 
  margin-top 150px
  width 70% #修改此处，本人为90%
```


按你自己想法修改，这三个办法可以综合使用。

