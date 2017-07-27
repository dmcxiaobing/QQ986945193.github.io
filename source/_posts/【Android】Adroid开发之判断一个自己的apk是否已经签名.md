---
title: Adroid开发中判断一个自己的apk是否已经签名 #文章页面上的显示名称，一般是中文
date: 2017-07-27 15:30:16 #文章生成时间，一般不改，当然也可以任意修改
categories: Android #分类
tags: [Java,Android,apk,Windows知识,eclipse,AndroidStudio] #文章标签，可空，多标签请用格式，注意:后面有个空格
description: Adroid开发中判断一个自己的apk是否已经签名
---
作者：程序员小冰 （转载请说明出处）

今天给大家带来一个知识点，那就是判断自己的android应用apk是否进行了签名。我这里是用的Windows

测试。首先，进入我们的jdk的安装目录。如这里是我的:`D:\Users\kaifagongju\Java\jdk1.7.0_79\bin`

然后，我们将需要进行测试的apk拷贝进去，然后利用jarsigner命令就可以判断了。当出现以下代码就

代表成功了：`jar 已验证。

警告:
此 jar 包含证书链未验证的条目。
此 jar 包含的签名没有时间戳。如果没有时间戳, 则在签名者证
7) 或以后的任何撤销日期之后, 用户可能无法验证此 jar。

有关详细信息, 请使用 -verbose 和 -certs 选项重新运行。`

下面给大家看一下截图吧:

![这里写图片描述](http://img.blog.csdn.net/20161125174549158)