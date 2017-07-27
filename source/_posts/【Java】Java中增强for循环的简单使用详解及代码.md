---
title: java中增强for循环的简单使用详解及代码 #文章页面上的显示名称，一般是中文
date: 2017-07-26 15:30:16 #文章生成时间，一般不改，当然也可以任意修改
categories: Java #分类
tags: [Java,android] #文章标签，可空，多标签请用格式，注意:后面有个空格
description: java中增强for循环的简单使用详解及代码
---
java中增强for循环的简单使用详解及代码
<!--more-->

For-Each 循环是 J2SE 5 中引入的，它是 for 循环的一种缩略形式，通过它可以简化复杂的 for 循环结构。For-Each 循环主要用在集合（如数组）中，按照严格的方式，从开始到结束循环，它的使用是非常方便的。

首先说一下他的语法结构：

```
for(数据类型  变量 ：集合){
	//这里写要遍历的元素，或者所需要的代码即可
}

```
下面是一个简单的demo示例：
```
  public class ForEach {
        public static void main(String[] args) {
            int sum = 0;
            int[] nums = {1, 2, 3, 4, 5, 6, 7, 8, 9, 0};
            for (int i : nums) {
                System.out.println("数组元素:" + i);
                sum += i;
            }
            System.out.println("数组元素和:" + sum);
        }
    }
```