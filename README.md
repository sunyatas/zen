# Uno Zen for Ghost

![Last version](https://img.shields.io/github/tag/bestswifter/uno-zen.svg?style=flat-square)
[![Build Status](http://img.shields.io/travis/Kikobeats/uno-zen/master.svg?style=flat-square)](https://travis-ci.org/Kikobeats/uno-zen)
![Ghost version](https://img.shields.io/badge/Ghost-0.8.x-brightgreen.svg?style=flat-square)
![Node version](https://img.shields.io/node/v/uno-zen.svg?style=flat-square)


> 感谢 Kikobeats 的主题 [Uno Zen](https://github.com/Kikobeats/uno-zen)，本主题由此改造而成
<br>
> **NOTE**: 商用版本可以在这里购买 [Uno Urban](https://sellfy.com/p/G5kK).

[<img src="http://i.imgur.com/LCSB4Ca.jpg">](http://kikobeats.com)

---

# 介绍

**Uno Zen** 是基于 [Uno](https://github.com/daleanthony/Uno) 开发的一个 Ghost 博客主题。它提供了功能和样式上一些小的改进和优化。

### 我对原主题的改动

* 使用 highlight.js 实现代码高亮
* 使用 [Font Awesome](http://fontawesome.io/) 管理社交按钮图标
* 快速集成 Disqus 评论管理系统
* 修改中文版 ghost 下，文章天数计算错误的bug

###你可以访问我的博客查看 [demo](https://bestswifter.com)

## 安装

首先确保你的服务器已经安装了 Git

进入 ghost 根目录下的 theme 文件夹(`path-to-ghost/content/themes`)，然后运行以下命令：

```bash
git clone https://github.com/bestswifter/uno-zen.git
```

重启 ghost 服务，进入后台就可以看到 Uno-zen 这个主题了。

## 准备工作

你需要使用 jQuery，不过我更推荐使用 [Zepto](https://github.com/madrobby/zepto)，这是一个轻量级的 jQuery 替代库，它完全兼容 jQuery：

```html
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/zepto/1.1.6/zepto.min.js"></script>
<script>jQuery = Zepto</script>
```

你需要把它添加到博客的 Footer 里面：

![](http://i.imgur.com/xUXdFeH.png)

## 更新

在 `themes/uno-zen` 目录下执行：

```bash
git pull origin
``` 

## 自定义

我对原主题做了一些改动，主要有：

### 代码高亮

采用 [highlight.js](https://highlightjs.org/) 做代码高亮，只需要修改 `default.hbs` 中的主题即可，默认采用 tomorrow 主题：

```js
<link rel="stylesheet" href="/highlight/styles/tomorrow.css">
```

### 社交按钮与图标

采用 [Font Awesome](http://fontawesome.io/) 的图标字体来展示社交按钮，请参考我的 `partials/social.hbs` 文件中的代码：

```html
<a href="https://github.com/bestswifter" title="@KtZhang 的 Github" target="_blank">
  <i class='social fa fa-github'></i>
  <span class="label">Github</span>
</a>

<a href="http://weibo.com/bestswifter" title="@bestswifter" target="_blank">
  <i class='social fa fa-weibo'></i>
  <span class="label">weibo</span>
</a>
```

如果你需要使用别的图片，只要去 [Font Awesome](http://fontawesome.io/) 官网查一查图片名即可。

### 头像与封面

封面图片可以直接在 ghost 后台进行配置。

使用 [Favicon Generator](http://realfavicongenerator.net/) 生成不同平台下的头像图片，并放入 `assets/img` 文件夹下。

### 文章列表的总标题

在[我的博客](https://bestswifter.com)中，你可以看到所有文章的最上方有一个大标题：**作品集**，如果你想换成别的名字，可以在 ghost 后台插入代码，在 `{{ghost_head}}` 中加入以下代码：

```js
<script>
var posts_headline = '作品集 ';
</script>
```

### Disqus 评论管理

只要在 `{{ghost_head}}` 中加入你的站点的 shortname 即可：

```js
<script>
var disqus_shortname = 'bestswifter'; // 改成自己的 shortname
</script>
```

### 时间统计

所有的文章都会显示 “xxx Days Ago”，表示这是你多久以前的文章。原来的代码似乎与中文版ghost不兼容，我做了一些修改，具体效果可以参考[我的博客](https://bestswifter.com)。

### 自定义导航页

你可以为你的博客配置多个导航页，比如 ”关于“ 页面。这个可以在 ghost 的后台进行配置。

### TODO

uno-zen 是一个非常优秀的主题，作者还在不断的对他进行更新，我也会不断探索新的功能并与大家分享。

## License

MIT © [bestswifter](https://bestswifter.com)
