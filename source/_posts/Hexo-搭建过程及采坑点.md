---
title: Hexo 搭建过程及采坑点
date: 2020-04-22 17:53:37
tags:
 - hexo
 - wizard
categories:
 - hexo
---

## 安装教程

- Git  
- NodeJS



## 基本使用

- hexo init [dirname]
- cd [dirname]
- npm install
- hexo new 
- hexo g[generate]
- hexo s[server] | --debug
- npm install hexo-deployer-git –save
- hexo d[deploy]



## 新建博客

- hexo new "blog name"
- 在本地`./source/_posts`文件夹下出现`blogname.md`文件，编辑文本和主要内容
- hexo clean
- hexo g
- hexo d



## 异地编辑

> 思路是根据不同分支处理不同的内容，master分支用于博客部署的静态资源；而hexo分支主要用于保存博客编辑中hexo的工作环境

- 按照同类环境
- 克隆代码-hexo分支
- 编辑文件--添加Git提交--hexo更新部署



---

## 少量坑

### 安装及配置

- Windows下安装尽量使用`cmd`执行`npm install -g hexo-cli `等命令，`PowerShell`或`Git Bash`执行有少量结果与显示信息异常
- `busuanzi`插件统计时，本地运行测试统计结果为脏值
- `Next`主题导航栏中的`tags|categories|about`等点击出现`Get /~/%20/`异常时，将`theme/next/_config.yml`内相关`menu`中的多余空格去掉
- 注意`Next-theme`的维护地址是否使用最新版本：[theme-next](https://github.com/theme-next/hexo-theme-next.git)

### 参考

- [WUGENQIANG](https://wugenqiang.github.io/articles/hexo-do-optimization.html)
- [NMASK](https://thief.one/2017/03/03/Hexo%E6%90%AD%E5%BB%BA%E5%8D%9A%E5%AE%A2%E6%95%99%E7%A8%8B/)
- [eternalzttz](http://eternalzttz.com/hexo-next.html)
- [hexo.io](https://hexo.io/zh-cn/)