---
layout: post
title:  Github Pages的使用
categories: Tools
description: Github Pages的使用
keywords: github Pages, blog
---

## 使用Github Pages快速搭建自己的网站  
参考[Github+Jekyll 搭建个人网站详细教程](https://www.jianshu.com/p/9f71e260925d)
### 最直接的方法
1. 在Github网站上创建一个名为**你的github账户名.github.io**的仓库  
2. 选择模板 或者 fork别人已有的仓库
3. 修改配置文件、界面


### 使用Jekyll搭建blog
#### _系统环境:_
+ os:*Windows10*  
+ [Ruby](https://rubyinstaller.org/downloads/)(ps:我的下载 2.6.3-1 (x64) )
	- 将安装的l=路径下的bin目录添加到系统变量(ps:我的路径：D:\DevTools\Ruby26-x64\bin)
	- `ruby -v`
+ [Gem](https://rubygems.org/pages/download)(-有的Ruby版本好像没有gem工具，需要自己安装)
  - 进入解压路径执行 `ruby setup.rb`
  - `gem -v`
+ Jekyll
	- `gem install jekyll`
	- `jekyll -v`
+ [Git](https://git-scm.com/downloads)

#### _创建网站:_
**测试**
+ 使用jekyll构建项目
	1. `jekyll new pro_name `
	2. 进入pro_name再执行：`jekyll serve` or `jekyll s`
	3. 往_post文件夹中放入格式为`yyyy-MM-dd-filename`的md文件，访问 `http://127.0.0.1:4000/` 浏览效果
+ 根据模板说明进行个性化设置
+ 将该项目推送到你新建的yourname.github.io仓库, 访问 `http://yourname.github.io` 浏览效果
**其他方法**
- 可以从jekyll下载新的网站模块[jekyllthemes](http://jekyllthemes.org/)  or [jekyllthemes-dev](https://jekyllthemes.dev/)

	+ if miss bundler:
	- `gem install bundler`
	- `bundle install`
	+ if oucces error:
	```
	  Conversion error: Jekyll::Converters::Scss encountered an error while converting 'assets/css/styles.scss':
                    Invalid GBK character "\xE2" on line 241
	```
	- Ruby21\lib\ruby\gems\2.1.0\gems\sass-3.4.15\lib\sass在文件中添加一行Encoding.default_external = Encoding.find('utf-8') *参考解决[ruby编译scss出现invalid GBK错误](https://segmentfault.com/a/1190000002932352)*
- 也可以clone别人的仓库，将仓库名改为yourname.github.io，进行配置

#### jekyll目录结构主要包含如下目录：
	_posts 博客内容
	_pages 其他需要生成的网页，如About页
	_layouts 网页排版模板
	_includes 被模板包含的HTML片段，可在_config.yml中修改位置
	assets 辅助资源 css布局 js脚本 图片等
	_data 动态数据
	_sites 最终生成的静态网页
	_config.yml 网站的一些配置信息
	index.html 网站的入口






