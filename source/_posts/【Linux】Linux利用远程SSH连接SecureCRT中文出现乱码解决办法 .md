---
title: Linux利用远程SSH连接SecureCRT中文出现乱码解决办法  #文章页面上的显示名称，一般是中文
date: 2017-07-26 15:30:16 #文章生成时间，一般不改，当然也可以任意修改
categories: Linux #分类
tags: [Linux] #文章标签，可空，多标签请用格式，注意:后面有个空格
description: Linux利用远程SSH连接SecureCRT中文出现乱码解决办法
---
Linux利用远程SSH连接SecureCRT中文出现乱码解决办法
<!--more-->

1. 修改远程linux机器的配置
 
　　vim /etc/sysconfig/i18n
 
　　把LANG改成支持UTF-8的字符集
 
　　如：
 
　　LANG=”zh_CN.UTF-8″
 
　　或者是
 
　　LANG=”en_US.UTF-8″
 
　　2. 改Secure CRT的设置
 
　　选项-》会话选项-》外观-》字符编码-》uft-8
 
　　3. 退出，重新登录。
 
　　utf8的文件与文件名均可以正常阅读了。
 
　　上面就是Linux下SecureCRT中文显示乱码的解决方法，如果你使用中文语言的SecureCRT时出现乱码，可按文中介绍的方法对LANG进行修改。
 