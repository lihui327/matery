---
title: 关于github+vercel+hexo搭建博客需要注意的事项
date: 2022-05-22 16:26:05
categories: blog
tags:
- github
- vercel
- hexo
---

首先我们需要注意的是要有模板，即能够适配vercel项目的文件结构，推荐直接到vercel+hexo的官方仓库下载整个仓库文件，网址[vercel/examples/hexo at main · vercel/vercel (github.com)](https://github.com/vercel/vercel/tree/main/examples/hexo).

<!-- more -->

#### 初始化

将下载下来的zip解压到你的博客目录，管理员模式下使用power shell进入到该目录，执行以下命令

`npm install hexo-cli -g`  一般情况下只用执行这一条命令即可

`npm install hexo-deployer-git --save`

#### 修改配置文件

因为官方仓库的配置文件可能有点老了，所以有些没有及时更新，所以需要通过`hexo g`+`hexo s`命令查看期中是否有些命令已弃用，并及时更新成新的配置文件，注意修改站点的网址，一般为https://仓库名.vercel.app

#### 创建仓库

建议不要直接在vercel上创建hexo项目，因为创建的仓库是main分支，对于本地git push操作会比较麻烦，建议先创建仓库并将本地博客文件push到新建的仓库下，命令如下：

```git
git init
git add --all
git commit -m "first commit"
git branch -M master	//第一次push时需要输入，之后不用
git remote add origin https://github.com/github用户名/仓库名.git
git push -u origin master	//第一次push使用此命令，之后push均使用下面的命令
git push --force origin master
```

#### 导入仓库

1. 进入vercel官网，如下图：

![](http://photo.lihui327.cn/blog/2022/2022-05-22_165042.png) 

2. 导入，默认即可，然后等待配置

![](http://photo.lihui327.cn/blog/2022/2022-05-22_165407.png) 

3. 完成，进入到网站看看，还不错-_-

![](http://photo.lihui327.cn/blog/2022/2022-05-22_165754.png)

#### Hexo

官网：<https://hexo.io>.

vercel+hexo：[lihui327/vercel_hexo (github.com)](https://github.com/lihui327/vercel_hexo).

vercel：<https://vercel.com>.