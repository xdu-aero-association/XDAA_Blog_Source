# Blog for R&D Department of XDU Aero Association

## 西电航协研发部GitHub检索博客

### Status

![Hexo Blog CI](https://github.com/uav-operation-system/XDAA_Blog_Source/workflows/Hexo%20Blog%20CI/badge.svg?branch=master)

![stars](https://img.shields.io/github/stars/uav-operation-system/XDAA_Blog_Source.svg) ![forks](https://img.shields.io/github/forks/uav-operation-system/XDAA_Blog_Source.svg) ![tag](https://img.shields.io/github/tag/uav-operation-system/XDAA_Blog_Source.svg) ![release](https://img.shields.io/github/release/uav-operation-system/XDAA_Blog_Source.svg) ![issues](https://img.shields.io/github/issues/uav-operation-system/XDAA_Blog_Source.svg)

### Description

该存储库存储uav-operation-system.github.io博客的源码

该博客目的是方便大家检索存储库中的资源，该博客仍处于待完善状态，未来会进一步推进与不断完善。

### Progress

|Tag|功能|完成日期|
|:-:|:-:|:-:|
|0.1.0|搭建最基本博客环境并线上构建成功|2020.05.08|
|0.1.1|创建博客核心页面|待定|
|0.1.2|添加导言区、页面自动跳转|待定|
|0.1.3|完善UI部分|待定|

## 注意事项

uav-operation-system.github.io存储库为博客后端数据库，请勿手动编辑内容。该内容通过hexo自动化部署。

本地查看部署后的源码请通过hexo server查看，默认端口号为4000。

更换主题时，请删除主题内的md文件（.开头的文件夹中的md文件不用删），否则可能会导致hexo自动化部署时报错。

由于uav-operation-system.github.io存储库的内容无法在本地运行，因此请勿克隆uav-operation-system.github.io存储库！

使用最新版Node进行hexo部署的时候会报错，请使用稳定版Node（目前使用的版本是Node 12）

本地自动化部署：安装hexo-deployer-git工具

安装方法如下：

```java
$ npm install hexo-deployer-git --save
```

GitHub自动化CI部署：采用GitHub Actions实现，每次git push后，CI会使用hexo d命令自动部署至uav-operation-system.github.io存储库

为了账户安全起见，CI自动化构建不存储用户密码，而是采用存储库的HEXO_DEPLOY_PRIVATE_KEY私钥通过ssh上传，请勿删除该私钥。

_config.yml这个文件后面的repo地址请使用git地址，否则CI自动化构建的时候会报错

配置如下（注意冒号后面要跟一个空格，否则会报错）：

```java
deploy:
  type: git
  repo: git@github.com:uav-operation-system/uav-operation-system.github.io.git
  branch: master
```

## 作者

博客主编：Phillweston
主编邮箱：2436559745@qq.com
