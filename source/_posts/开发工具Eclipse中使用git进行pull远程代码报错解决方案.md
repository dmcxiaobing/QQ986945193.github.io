---
title: Eclipse中使用git进行pull远程代码报错解决方案 #文章页面上的显示名称，一般是中文
date: 2017-07-26 15:30:16 #文章生成时间，一般不改，当然也可以任意修改
categories: 开发工具 #分类
tags: [Java,Android,git,github,Windows知识,eclipse,myeclipse] #文章标签，可空，多标签请用格式，注意:后面有个空格
description: Eclipse中使用git进行pull远程代码，报错The current branch is not configured for pull No value for key
---

当使用eclipse或者MyEclipse进行pull远程代码的时候，或者github的代码的时候报如下错误代码；

代表我们没有配置我们的git地址，这里我教大家配置一下。首先下面是错误代码：
```
The current branch is not configured for pull
No value for key branch.master.merge found in configuration
```

解决方法：

1. 在我们本地工程目录找到config文件（如我的是E:\david\xiaobing\.git）；

2. 修改config文件内容为：

```
[core]
    repositoryformatversion = 0
    filemode = false
    logallrefupdates = true
    [branch "master"] 
        remote = origin 
        merge = refs/heads/master 
    [remote "origin"] 
        url = https://github.com/QQ986945193/DavidAndroidProjectTools.git
		        （修改为自己的url,然后去掉此括号中的内容即可）
        fetch = +refs/heads/*:refs/remotes/origin/*
        
```

3. 最后再执行pull方法，发现工作ok了