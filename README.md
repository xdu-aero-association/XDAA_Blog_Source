# Blog for R&D Department of XDU Aero Association

## 西电航协研发部GitHub检索博客

### Status

![Hexo Blog CI](https://github.com/xdu-aero-association/XDAA_Blog_Source/workflows/Hexo%20Blog%20CI/badge.svg?branch=master)

![stars](https://img.shields.io/github/stars/xdu-aero-association/XDAA_Blog_Source.svg) ![forks](https://img.shields.io/github/forks/xdu-aero-association/XDAA_Blog_Source.svg) ![tag](https://img.shields.io/github/tag/xdu-aero-association/XDAA_Blog_Source.svg) ![release](https://img.shields.io/github/release/xdu-aero-association/XDAA_Blog_Source.svg) ![issues](https://img.shields.io/github/issues/xdu-aero-association/XDAA_Blog_Source.svg)

### Description

该存储库存储xdu-aero-association.github.io博客的源码

该博客目的是方便大家检索存储库中的资源，该博客仍处于待完善状态，未来会进一步推进与不断完善。

### Progress

|Tag|功能|完成日期|
|:-:|:-:|:-:|
|0.1.0|搭建最基本博客环境并线上构建成功|2020.05.08|
|0.1.1|创建博客核心页面|待定|
|0.1.2|添加导言区、页面自动跳转|待定|
|0.1.3|完善UI部分|待定|

## 注意事项

xdu-aero-association.github.io存储库为博客后端数据库，请勿手动编辑内容。该内容通过hexo自动化部署。

本地查看部署后的源码请通过hexo server查看，默认端口号为4000。

更换主题时，请删除主题内的md文件（.开头的文件夹中的md文件不用删），否则可能会导致hexo自动化部署时报错。

由于xdu-aero-association.github.io存储库的内容无法在本地运行，因此请勿克隆xdu-aero-association.github.io存储库！

## Hexo博客部署方法

使用最新版Node进行hexo部署的时候会报错，请使用LTS稳定版Node（目前使用的版本是Node 12）

本地自动化部署：安装hexo-cli和hexo-deployer-git工具

安装方法如下：

0. 切换到国内淘宝镜像源以加快安装速度

```java
$ npm --registry https://registry.npm.taobao.org info underscore
```

1. 执行以下命令进行Hexo框架的基本安装

```java
$ npm install hexo-cli -g
```

2. 安装便于自动部署到Github上的插件

```java
$ npm install hexo-deployer-git --save
```

3. 安装atom生成插件，便于感兴趣的小伙伴们订阅

```java
$ npm install hexo-generator-feed --save
```

4. 安装博客首页生成插件

```java
$ npm install hexo-generator-index --save
```

5. 安装归档生成插件

```java
$ npm install hexo-generator-archive --save
```

6. 安装tag生成插件

```java
$ npm install hexo-generator-tag --save
```

7. 安装category生成插件

```java
$ npm install hexo-generator-category --save
```

8. 安装Sitemap文件生成插件

```java
$ npm install hexo-generator-sitemap --save
```

9. 安装百度Sitemap文件生成插件，因为普通的Sitemap格式不符合百度的要求

```java
$ npm install hexo-generator-baidu-sitemap --save
```

GitHub自动化CI部署：采用GitHub Actions实现，每次git push后，CI会使用hexo d命令自动部署至xdu-aero-association.github.io存储库

为了账户安全起见，CI自动化构建不存储用户密码，而是采用存储库的HEXO_DEPLOY_PRIVATE_KEY私钥通过ssh上传，请勿删除该私钥。

_config.yml这个文件后面的repo地址请使用git地址，否则CI自动化构建的时候会报错

配置如下（注意冒号后面要跟一个空格，否则会报错）：

```java
deploy:
  type: git
  repo: git@github.com:xdu-aero-association/xdu-aero-association.github.io.git
  branch: master
```

[Hexo添加emoji表情](https://blog.csdn.net/weixin_30745641/article/details/95686757)

首先要卸载hexo默认的marked渲染器，安装markdown-it渲染器，之后安装markdown-it-emoji插件，运行的命令如：

```java
npm un hexo-renderer-marked --save
npm i hexo-renderer-markdown-it --save
npm install markdown-it-emoji --save
```

而后安装twemoji（原有的emoji样式不美观）

```java
npm install twemoji
```

[Hexo添加gitalk评论功能](https://www.izhongxia.com/posts/41249.html)

[Hexo添加后台访问量统计功能](https://blog.qust.cc/archives/48665.html)

**注意：**

1. 该功能不能与valine在线评论功能同时开启，若同时安装了Valine评论系统会产生冲突。

2. 由于Hexo更新了security机制，因此原leancloud添加机制失效，详情请查看下面链接

3. 如果不关注security信息，可设置为false

[Hexo添加valine在线评论功能](https://zhuanlan.zhihu.com/p/115156647)

## Hexo常见问题

[hexo引用本地图片无法显示](https://blog.csdn.net/xjm850552586/article/details/84101345)

[Github Actions 通过 SSH 自动部署 Hexo](https://blog.csdn.net/z_johnny/article/details/103910373)

## 作者

博客主编：Phillweston

主编邮箱：2436559745@qq.com
