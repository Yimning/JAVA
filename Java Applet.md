<!--
 * @Author: Yimning
 * @Date: 2021-01-15 12:24:52
 * @LastEditTime: 2021-02-15 14:00:02
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit  
 * @FilePath: \undefinedc:\Users\Yimning\Desktop\JAVA\Java Applet.md
-->

# Applet  

## 1、Applet简介

​	●Java程序可分为Application和Applet两种类型。Application程序就是前面各章中我们看到的带有main0方法的程序，又称之为Java应用程序。Applet程序又称之为小应用程序，是指能够在其他应用程序(通常是网页浏览器)中执行的Java程序，并不是指Applet程序就非得是代码量小的一个小程序。

  ●要编写Applet程序，需要继承java.applet.Applet类或javax.swing.JApplet类。
[例1]一个简单的Applet程序。
		java. lang. Object
			L java. awt. Component
				L java. awt. Container
					L java. awt. Panel
						L java. applet. Applet
							L javax. swing. JApplet （swing是轻量级的图形用户组件） 

## 2、Applet的运行

​	●Applet程序需要嵌入到网页中运行。网页是由一种称作HTML (HyperText Markup Language)的语言编写的。.

​	●Applet程序除了可以在浏览器中运行以外，也可通过Java开发工具包(Java Development Kit)所自带的appletviewer程序来运行。

●在Eclipse开发工具中，提供了能够直接创建和运行Applet程序的功能。

●HTML与Applet
[例2]用HTML语言编写一个网页的基本结构如下:

```
    <HTML>
    <HEAD>
    <TITLE>pagc-tit1c</TITLE>
    </HEAD>
    <BODY>
       pagC- -contents
    </B0DY>
    </HTML>
``` 
●HTML与Applet 	

​	●<applet>标记用于在网页中钳入applet程序如:

```
<applet code="HelloJavaApplet" width=200 height=50> </applet>
```

​	●将在网页中类名为HelloJavaApplet的applet<applet>标记中可包含子标记<param>，用于向applet程序
提供参数，如:< param name="param- -name" value=" param-value" >在applet程序中可通过调用方法: getParameter (String paramName)，获得参数值。

​	在appletvi ewer中运行Applet程序appletviewer: JDK自 带的调试工具
​	命令格式: appletviewer <HTM文件>
​	使用appletviewer的快捷方式，需要在Applet源程序顶部以注释方式加入<applet>标记

​	●网页浏览器对运行Applet程序都从安全角度设置了一些限制。不同的网页浏览器对applet运行所设置的限制略有所不同。但基本上来说都会禁止未经认可的代码访问本地文件系统，以及禁止未经认可的代码进行某些网络操作。这些都是非常必要的。否则，黑客就可以很容易地通过一个Applet程序，读取客户存放在本地计算机.上的机密资料，并通过网络传送到其他计算机。  
## 3、Applet的生命周期

![1609571635693](C:\Users\Yimning\AppData\Roaming\Typora\typora-user-images\1609571635693.png)

## 4、 Applet的其他功能

​	●Applet本身是-一个AWT组件，因此它也具有一般AWT组件的图形绘制功能。Applet程序中所采用的AWT绘图机制主要涉及三个方法: paint()、update0和repaint0方法。update(方法和paint()方法都有一个Graphics类的参数。Graphics类 是画图的关键，它可以支持两种绘图方式:一 种是基本的绘图，如:画线、矩形、圆等;另一种是画图像，主要用于动画制作。

​	●在Applet中播放声音可以通过java.applet.AudioClip接 口来实现。在AudioClip接口中声明“了如下三个方法用于播放声音:
​		●void play(:用于播放声音。
​		●void loop0:循环播放声音。
​		●void stopO:停止播放声音。

​	●有时JavaApplet中需要显示--些图像(如GIF文件)。显示图像需要先定义一个Image类的对象，然后使用Applet类的getImage(方法把图像文件和Image对象关联起来。Graphics类 的drawImage(方法用来显示Image对象。为了提高显示质量，一般Applet中都首先把图像装入内存，然后再显示在屏幕上。