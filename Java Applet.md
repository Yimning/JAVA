<!--
 * @Author: Yimning
 * @Date: 2021-01-15 12:24:52
 * @LastEditTime: 2021-02-09 12:58:06
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