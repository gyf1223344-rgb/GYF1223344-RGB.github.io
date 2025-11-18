_site/
*.sw[po]
*.~vsd
\#*\#
*~
.DS_Store
Gemfile.lock
.vscode/
.jekyll-metadata
.\$*.png.bkp
.\$*.png.dtmp

# ---------------- #
#   Main Configs   #
# ---------------- #
baseurl:
url: https://mazhuang.org
date_format: "ordinal"
title: 码志
subtitle: "公众号：闷骚的程序员"
description: "马壮的个人博客，公众号：闷骚的程序员"
keywords: 码志, Zhuang Ma, mzlogin, mazhuang, 闷骚的程序员
timezone: Asia/Shanghai
encoding: "utf-8"
# 页面左下角显示的年份
since: 2015
# 源码仓库，请替换成自己的
repository: mzlogin/mzlogin.github.io
# 对 css 和 js 资源的 cdn 加速配置
cdn:
    jsdelivr:
        enabled: false
# 可选组件配置
components:
    # 分享
    # weibo,qq,wechat,douban,qzone,linkedin,facebook,twitter
    share:
        enabled: false
        hide-platforms: qq,facebook
    # 不蒜子访问统计
    busuanzi:
        enabled: false
        start_date: 2020-05-03
    # My Popular Repositories
    side_bar_repo:
        enabled: true
        limit: 5
    # 文章字数统计
    word_count:
        enabled: true
    # 页面右上角，以及「关于」页面的二维码
    # 修改图片请替换 assets/images/qrcode.jpg
    qrcode:
        enabled: true
        image_alt: 闷骚的程序员
    # 维基索引页使用哪种视图，支持 列表（list）/分类（cate）
    wiki:
        view: cate
    # 图片灯箱效果功能
    fancybox:
        enabled: false
# 压缩页面内容
compress_html:
  clippings: all
  comments: ["<!--", "-->"]
# 代码高亮风格，支持的 theme 列表见 https://github.com/mzlogin/rouge-themes
highlight_theme: github

# ---------------- #
#      Author      #
# ---------------- #
author: Zhuang Ma
organization: 
organization_url: 
github_username: mzlogin
location: Wuhan, China
email: chumpma@gmail.com

# ---------------- #
#    Navigation    #
# ---------------- #
navs:
  -
    href: /
    label: 首页

  -
    href: /categories/
    label: 分类

  -
    href: /archives/
    label: 归档
    mobile-hidden: true

  -
    href: /open-source/
    label: 开源
    mobile-hidden: true

  -
    href: /fragments/
    label: 片段

  -
    href: /wiki/
    label: 维基

  -
    href: /links/
    label: 链接
    mobile-hidden: true

  -
    href: /about/
    label: 关于

# ---------------- #
#       RSS        #
# ---------------- #
subscribe_rss: /feed.xml

# ---------------- #
#      INDEX       #
# ---------------- #
index:
    banner:
        # 首页 banner 区文字颜色
        color: "#fff"
        # 首页导航栏文字颜色
        nav-color: "rgba(255, 255, 255, .5)"
        # 首页 banner 区背景颜色
        background-color: "#4183c4"
        # 首页 banner 区背景图片
        # background-image: "/assets/images/octicons-bg.png"
        # background-repeat: "no-repeat"
        # background-size: "cover"

# ---------------- #
#      Jekyll      #
# ---------------- #
markdown: kramdown
kramdown:
    input: GFM
highlighter: rouge
paginate: 10
lsi: false
quiet: false
excerpt_separator: "\n\n"
permalink: /:year/:month/:day/:title/
plugins:
    - jekyll-github-metadata
    - rouge
#     - jekyll-html-pipeline
    - jekyll-paginate
    - jekyll-sitemap
    - jekyll-feed
    - jemoji
#     - jekyll-mentions
collections:
    wiki:
        output: true
        permalink: /wiki/:path/
    fragments:
        output: true
        permalink: /fragment/:path/

# ---------------- #
#      Comments    #
# ---------------- #
# support provider: disqus, gitment, gitalk, utterances, beaudar, giscus
comments_provider: giscus
# !!!重要!!! 请修改下面这些信息为你自己申请的
# !!!Important!!! Please modify infos below to yours
# disqus 配置参考：https://disqus.com
disqus:
    username: 
# gitment 配置参考：https://imsun.net/posts/gitment-introduction/
gitment:
    owner: mzlogin
    repo: blog-comments
    oauth:
        client_id: d2e1cbbd298958076462
        client_secret: b42a4178e5fd4a7cf63189ef4b1453b05c375709
# gitalk 配置参考：https://github.com/gitalk/gitalk#install
gitalk:
    owner: mzlogin
    repo: blog-comments
    clientID: d2e1cbbd298958076462
    clientSecret: b42a4178e5fd4a7cf63189ef4b1453b05c375709
# utterances 配置参考：https://utteranc.es/
utterances:
    repo: mzlogin/blog-comments
# beaudar 配置参考：https://beaudar.lipk.org/
beaudar:
    repo: mzlogin/blog-comments
# giscus 配置参考：https://giscus.app/zh-CN
giscus:
    repo: mzlogin/blog-comments
    repo-id: MDEwOlJlcG9zaXRvcnk5MzEyNzkxNw==
    category: Announcements
    category-id: DIC_kwDOBY0E7c4CRtg9
# 在使用其它评论组件时可点击显示 Disqus
lazy_load_disqus : false

# ---------------- #
#      Search      #
# ---------------- #
simple_jekyll_search:
    # 是否支持全文搜索
    fulltext: false
    # 最多显示多少条搜索结果
    limit: 10

# ---------------- #
#      Google      #
# ---------------- #
google:
    analytics_id: # G-20FLEG5Q2W
    adsense:
        enabled: true
        footer: true
        sidebar: true
        sidebar-detail: true
        content_header: false
        content_footer: false

google.com, pub-7093222719567591, DIRECT, f08c47fec0942fa0
mazhuang.org
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw]
gem 'wdm', '>= 0.1.0' if Gem.win_platform?

gem "webrick", "~> 1.7"

---
layout: default
class: home
comments: false
---

<style>
.home .banner,
.home .site-header,
.home .banner .collection-head,
.home .banner .collection-head a,
.home .site-header h1 a,
.home .site-header .site-header-nav-item:hover {
    color: {{ site.index.banner.color | default: '#fff' }};
}

.home .site-header .site-header-nav-item {
    color: {{ site.index.banner.nav-color | default: 'rgba(255, 255, 255, .5)' }};
}

.home .banner,
.home .site-header {
    background-color: {{ site.index.banner.background-color | default: '#4183c4'}};
}

{% if site.index.banner.background-image %}
.home .banner {
    background-image: url("{{ site.index.banner.background-image }}");
    background-repeat: {{ site.index.banner.background-repeat | default: 'no-repeat' }};
    background-size: {{ site.index.banner.background-size | default: 'cover' }};
}
{% endif %}

.home .banner .collection-head {
    background: 0 0;
    box-shadow: none;
    -webkit-box-shadow: none
}

.home .site-header {
    border-bottom: none
}

@media (max-width:50em) {
  .home .collapsed .icon-bar {
    background-color: white;
  }

  .home .collection-head .collection-header {
    font-size: 1.25em;
  }
}
</style>

{% assign assets_base_url = site.url %}
{% if site.cdn.jsdelivr.enabled %}
{% assign assets_base_url = "https://fastly.jsdelivr.net/gh/" | append: site.repository | append: '@master' %}
{% endif %}
<section class="banner">
    <div class="collection-head">
      <div class="container">
        <div class="columns">
          <div class="column two-thirds">
            <div class="collection-title">
              <h1 class="collection-header" id="sub-title"><span>{{ site.subtitle }}</span></h1>
              <div class="collection-info">
                <span class="meta-info mobile-hidden">
                  <span class="octicon octicon-location"></span>
                  {{ site.location }}
                </span>
                {% if site.organization %}
                <span class="meta-info">
                  <span class="octicon octicon-organization"></span>
                  <a href="{{ site.organization_url }}" target="_blank">{{ site.organization }}</a>
                </span>
                {% endif %}
                <span class="meta-info">
                  <span class="octicon octicon-mark-github"></span>
                  <a href="https://github.com/{{ site.github_username }}" target="_blank">{{ site.github_username }}</a>
                </span>
              </div>
            </div>
          </div>
          <div class="column one-third mobile-hidden">
            <div class="collection-title">
              {% include sidebar-qrcode.html %}
            </div>
          </div>
        </div>
      </div>
    </div>
</section>
<!-- /.banner -->
<section class="container content">
    <div class="columns">
        <div class="column two-thirds" >
            <ol class="repo-list">
              {% for post in site.posts %}
              {% if paginator.page == 1 %}
              {% if post.topmost == true %}
              <li class="repo-list-item">
                <h3 class="repo-list-name">
                  <a href="{{ site.url }}{{ post.url }}"><span class="top-most-flag">[置顶]</span>{{ post.title }}</a>
                </h3>
                <p class="repo-list-description">
                {{ post.excerpt | strip_html | strip }}
                </p>
                <p class="repo-list-meta">
                <span class="meta-info">
                  <span class="octicon octicon-calendar"></span> {{ post.date | date: "%Y/%m/%d" }}
                </span>
                {% for cat in post.categories %}
                <span class="meta-info">
                  <span class="octicon octicon-file-directory"></span>
                  <a href="{{ site.url }}/categories/#{{ cat }}" title="{{ cat }}">{{ cat }}</a>
                </span>
                {% endfor %}
                </p>
              </li>
              {% endif %}
              {% endif %}
              {% endfor %}

              {% for post in paginator.posts %}
              {% if post.topmost != true %}
              <li class="repo-list-item">
                <h3 class="repo-list-name">
                  <a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
                </h3>
                <p class="repo-list-description">
                {{ post.excerpt | strip_html | strip }}
                </p>
                <p class="repo-list-meta">
                <span class="meta-info">
                  <span class="octicon octicon-calendar"></span> {{ post.date | date: "%Y/%m/%d" }}
                </span>
                {% for cat in post.categories %}
                <span class="meta-info">
                  <span class="octicon octicon-file-directory"></span>
                  <a href="{{ site.url }}/categories/#{{ cat }}" title="{{ cat }}">{{ cat }}</a>
                </span>
                {% endfor %}
                </p>
              </li>
              {% endif %}
              {% endfor %}
            </ol>
        </div>
        <div class="column one-third">
            {% include sidebar-search.html %}
            {% include sidebar-categories-cloud.html %}
            {% include sidebar-ad.html %}
            {% include sidebar-popular-repo.html %}
        </div>
    </div>
    <div class="pagination text-align">
      <div class="btn-group">
        {% if paginator.previous_page %}
          {% if paginator.previous_page == 1 %}
              <a href="{{ site.url }}/" class="btn btn-outline">&laquo;</a>
          {% else %}
              <a href="{{ site.url }}/page{{paginator.previous_page}}"  class="btn btn-outline">&laquo;</a>
          {% endif %}
        {% else %}
            <button disabled="disabled" href="javascript:;" class="btn btn-outline">&laquo;</button>
        {% endif %}

        {% if paginator.page == 1 %}
            <a href="javascript:;" class="active btn btn-outline">1</a>
        {% else %}
            <a href="{{ site.url }}/"  class="btn btn-outline">1</a>
        {% endif %}

        {% assign aroundSize = 2 %}
        {% assign midStartPage = paginator.page | minus: aroundSize %}
        {% if 2 > midStartPage %}
            {% assign midStartPage = 2 %}
        {% endif %}
        {% assign midEndPage = paginator.page | plus: aroundSize %}
        {% if midEndPage >= paginator.total_pages %}
            {% assign midEndPage = paginator.total_pages | minus:1 %}
        {% endif %}
        {% assign tmpPage = aroundSize | plus: 2 %}
        {% if paginator.page > tmpPage %}
          <button disabled="disabled" href="javascript:;" class="btn btn-outline">...</button>
        {% endif %}

        {% for count in (midStartPage..midEndPage) %}
          {% if count == paginator.page %}
            <a href="jaavascript:;" class="active btn btn-outline">{{count}}</a>
          {% else %}
            <a href="{{ site.url }}/page{{count}}"  class="btn btn-outline">{{count}}</a>
          {% endif %}
        {% endfor %}

        {% assign tmpPage = paginator.page | plus: aroundSize | plus: 1 %}
        {% if paginator.total_pages > tmpPage %}
          <button disabled="disabled" href="javascript:;" class="btn btn-outline">...</button>
        {% endif %}

        {% if paginator.total_pages > 1 %}
          {% if paginator.page == paginator.total_pages %}
              <a href="jaavascript:;" class="active btn btn-outline">{{paginator.total_pages}}</a>
          {% else %}
              <a href="{{ site.url }}/page{{paginator.total_pages}}"  class="btn btn-outline">{{paginator.total_pages}}</a>
          {% endif %}
        {% endif %}

        {% if paginator.next_page %}
            <a href="{{ site.url }}/page{{paginator.next_page}}"  class="btn btn-outline">&raquo;</a>
        {% else %}
            <button disabled="disabled" href="javascript:;" class="btn btn-outline">&raquo;</button>
        {% endif %}
        </div>
    </div>
    <!-- /pagination -->
</section>
<!-- /section.content -->

The MIT License (MIT)

Copyright (c) 2013 Zhuang Ma

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# 码志

我的个人博客：<https://mazhuang.org>，欢迎 Star 和 Fork。

## 概览

<!-- vim-markdown-toc GFM -->

* [效果预览](#效果预览)
* [Fork 指南](#fork-指南)
* [使用文档](#使用文档)
* [经验与思考](#经验与思考)
* [联系我](#联系我)
* [致谢](#致谢)

<!-- vim-markdown-toc -->

## 效果预览

**[在线预览 &rarr;](https://mazhuang.org)**

![screenshot home](https://mazhuang.org/assets/images/screenshots/home.png)

## Fork 指南

Fork 本项目之后，还需要做一些事情才能让你的页面「正确」跑起来。

1. 正确设置项目名称与分支。

   按照 GitHub Pages 的规定，名称为 `username.github.io` 的项目的 master 分支，或者其它名称的项目的 gh-pages 分支可以自动生成 GitHub Pages 页面。

2. 修改域名。

   如果你需要绑定自己的域名，那么修改 CNAME 文件的内容，并参考 [配置 GitHub Pages 站点的自定义域](https://docs.github.com/cn/pages/configuring-a-custom-domain-for-your-github-pages-site) 做好配置；如果不需要绑定自己的域名，那么删掉 CNAME 文件。

3. 修改配置。

   网站的配置基本都集中在 \_config.yml 文件中，将其中与个人信息相关的部分替换成你自己的，比如网站的 url、title、subtitle 和第三方评论模块的配置等。

   **评论模块：** 目前支持 disqus、gitment、gitalk、utterances、beaudar 和 giscus，选用其中一种就可以了，推荐使用 giscus。它们各自的官方配置指南链接在 \_config.yml 文件的 Comments 一节里都贴出来了，请参考官方指南配置。

   **注意：** 如果使用 disqus，因为 disqus 处理用户名与域名白名单的策略存在缺陷，请一定将 disqus.username 修改成你自己的，否则请将该字段留空。我对该缺陷的记录见 [Issues#2][3]。

4. 删除我的文章与图片。

   如下文件夹中除了 template.md 文件外，都可以全部删除，然后添加你自己的内容。

   * \_posts 文件夹中是我已发布的博客文章。
   * \_drafts 文件夹中是我尚未发布的博客文章。
   * \_wiki 文件夹中是我已发布的 wiki 页面。
   * \_fragments 文件夹中是我已发布的短文片段。
   * images 文件夹中是我的文章和页面里使用的图片。

5. 修改「关于」页面。

   pages/about.md 文件内容对应网站的「关于」页面，里面的内容多为个人相关，将它们替换成你自己的信息，包括 \_data 目录下的 skills.yml 和 social.yml 文件里的数据。

   skills.yml 和 social.yml 里内容的含义可以参考：[_data 目录下的 yml 文件内容含义](https://mazhuang.org/2020/05/03/blog-template-qna/#_data-%E7%9B%AE%E5%BD%95%E4%B8%8B%E7%9A%84-yml-%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9%E5%90%AB%E4%B9%89)。

## 使用文档

- [本博客模板常见问题 Q & A](https://mazhuang.org/2020/05/03/blog-template-qna/)。

- 在本地预览博客效果可以参考 [Setting up your Pages site locally with Jekyll][2]。

## 经验与思考

* 排版建议遵照一定的规范，推荐 [中文文案排版指北（简体中文版）][1]。

* 简约，尽量每个页面都不展示多余的内容。

* 有时一图抵千言，有时可能只会拖慢网页加载速度。

* 言之有物，不做无痛之呻吟。

* 如果写技术文章，那先将技术原理完全理清了再开始写，一边摸索技术一边组织文章效率较低。

* 杜绝难断句、难理解的长句子，如果不能将其拆分成几个简洁的短句，说明脑中的理解并不清晰。

* 可以学习一下那些高质量的博主，他们的行文，内容组织方式，有什么值得借鉴的地方。

## 联系我

如果对本博客模板或者内容有任何建议，可以通过 [Issues](https://github.com/mzlogin/mzlogin.github.io/issues) 或者微信公众号「闷骚的程序员」与我取得联系。

<img width="192px" height="192px" src="https://mazhuang.org/assets/images/qrcode.jpg"/>

## 致谢

本博客外观基于 [DONGChuan](https://dongchuan.github.io) 修改，感谢！

[1]: https://github.com/mzlogin/chinese-copywriting-guidelines
[2]: https://help.github.com/articles/setting-up-your-pages-site-locally-with-jekyll/
[3]: https://github.com/mzlogin/mzlogin.github.io/issues/2
