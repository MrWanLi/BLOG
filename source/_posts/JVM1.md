---
title: JVM入门class文件格式
date: 2020-10-22 10:10:09
categories: [programme]
tags: [JVM]
index_img: /img/logo/jvm.jpg 
banner_img: /img/bg/omid-armin-MDbl7S8yp60-unsplash.jpg
excerpt: JVM(一)
---
### jvm

***
#### JVM 即时编译
![JVM 即时编译](/img/jvm/JAVA编码执行.jpg)

***
#### JVM 实现
![JVM 实现](/img/jvm/JVM实现.jpg)
[Hotspot](https://www.oracle.com/technetwork/cn/java/javase/tech/index-jsp-136373-zhs.html)
[jrockit](https://www.oracle.com/middleware/technologies/jrockit/jrockit-mission-control.html)
[J9](https://www.ibm.com/support/knowledgecenter/en/SSYKE2_7.0.0/com.ibm.java.lnx.70.doc/user/java_jvm.html)
[TaobaoVM](http://jvm.taobao.org/)
[LiquidVM](https://docs.oracle.com/cd/E11035_01/wloc10/lvm/index.html)
[Azul VM ](https://www.azul.com/)

***
#### JVM 跨平台
![JVM 跨平台 ](/img/jvm/JVM.jpg)

***
#### JVM JRE JDK
![JVM JRE JDK](/img/jvm/JDKJREJVM.jpg)

***
####  JAVA语言和虚拟机规范
[JAVA语言和虚拟机规范 PDF](https://docs.oracle.com/javase/specs/index.html)


***
### class
#### class文件结构
![class文件结构](/img/jvm/class文件结构.jpg)

***
#### classFileFormat
二进制字节流
数据类型：u1,u2,u4,u8 和_info(类型)
+ info 来源hotspot源码中的写法
查看16进制格式classFile
+ sublime 
+ notepad++
+ IDEA插件 BinEd
观察ByteCode方法
+ javap
+ IDEA插件 JBE
+ IDEA插件 JClasslib
classfile构成
ClassFile {
    u4 magic;
    u2 minor_version;
    u2 magor_version;
    u2 constant_pool_count;
    u2 cp_info constant_pool[constant_pool_count - 1];
    u2
}



***
#### class怎么读
16进制读取JDK1.8
![16进制读取JDK1.8](/img/jvm/16进制读取JDK1.8.jpg)

java汇编
![java汇编](/img/jvm/java汇编.jpg)

class字典
![class字典](/img/jvm/class字典.png)

[JVM虚拟机规范](https://docs.oracle.com/javase/specs/jvms/se8/jvms8.pdf)

jvm八大原子操作
lock(锁定)  unlock(解锁)
read(读取)  write(写入)
load(载入)  store(存储)
use(使用)   assign(赋值)