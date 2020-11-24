---
title: 详解Class加载过程
date: 2020-11-02 15:29:06
categories: [programme]
tags: [JVM]
index_img: /img/logo/jvm.jpg 
banner_img: /img/bg/omid-armin-MDbl7S8yp60-unsplash.jpg
excerpt: JVM(二)
---

### class

***
####  class加载过程
![class从硬盘到内存](/img/jvm/class从硬盘到内存.jpg)
> 第一步 loading: 将class文件load进内存，一个个二进制的字节格式
>
> 第二步 linking:
                1.校验是否符合class文件标准
                2.class文件静态变量赋默认值
                3.class文件常量池里面的引用变成直接内存地址
>               
> 第三步 initializing: class文件静态变量赋初始值


####  双亲委派机制
> ![双亲委派机制](/img/jvm/双亲委派机制.jpg)

> 第一: 父加载器不是加载器的价值器，也不是加载器的父类加载器
> 第二: 通过双亲委派安全机制，jvm定义好的类不能被修改
> 第三:         
        1.Bootstrap ClassLoader加载路径：sun.boot.class.path
        2.Extension ClassLoader加载路径：java.ext.dirs
        3.App ClassLoader加载路径：java.class.path
