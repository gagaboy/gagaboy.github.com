---
layout: post
title:  "【原创】使用Intellij IDEA 13 搭建 moqui 开发环境"
date: 2014-05-25 17:18:32 +0800
comments: true
categories: moqui
---


都说 **Intellij IDEA** 是个神器，并且老戴童鞋也是用这个开发的moqui。为了方便的学习moqui，偶特地整了下这个号称最智能的IDE的环境，作为自己备忘以及其他感兴趣的童鞋们搭建环境参考（偶滴系mac，win下搭建方式差不多）。

下面一步步的讲解下如何快速让你的开发环境和moqui融合起来。

<!--more-->

1. 首先选择导入工程，选择工程目录，然后选择下图显示导入 _外部Gradle模块_ ：  
	   
	![import project][image-1]

2. 这里注意在mac下Intellij 13的gradle 有版本要求，至少 **1.10** 及以上版本：  
	   
	![gradleVersion][image-2]


3. 项目结构配置：基本上不用怎么改动，Intellij 很智能的把一些问题给处理掉了。当然，你也可以自己定制下，我个人是把一些输出目录在工程里面屏蔽了：
	   
	![config][image-3]

4. 然后，就是运行或者调试配置了：这个也很简单，**Edit Configurations…** 下添加 _groovy_ 的配置，每个配置是一个运行脚本。基本上 _moqui_ 只需要四个常用的（ **cleanAll** 、 **build** 、 **load** 、 **run** ）都给配上就可以了：

	![runConf][image-4]
	  
	![idea][image-5]

5. 基本完成这些配置就可以了，IDE环境已搭建好了，开始你的**_ moqui 之旅 _**吧....


[image-1]:	/moquiImgs/2014-05-25-moqui-with-intellij/import.png "import project"
[image-2]:	/moquiImgs/2014-05-25-moqui-with-intellij/gradleV10.png "gradleVersion"
[image-3]:	/moquiImgs/2014-05-25-moqui-with-intellij/config.png "config"
[image-4]:	/moquiImgs/2014-05-25-moqui-with-intellij/runConf.png "runConf"
[image-5]:	/moquiImgs/2014-05-25-moqui-with-intellij/idea.png "idea"