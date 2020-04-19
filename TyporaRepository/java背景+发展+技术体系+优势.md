# java背景 / 发展 / 技术体系 / 优势
### 1.计算机语言发展史
![java语言发展](otherSource\java语言发展.png)
<font  color=#808080 size=1> <源文件：[java语言发展.drawio](otherSource) ></font>

### 2.java的简介与发展历史背景
##### （1）简介
​		java是一种广泛使用的计算机编程语言，拥有跨平台、面向对象、泛型编程的特性，广泛应用于企业级Web应用开发和移动应用开发。

##### （2）起源与发展历程
​		Sun 公司（Stanford University Network/太阳计算机系统有限公司/昇阳电脑公司）的 James Gosling（詹姆斯·高斯林）等人于1990年代初开发 Java 语言的雏形，命名为Oak，目标设置在家用电器等小型系统的编程语言，应用于电视机、电话、闹钟、烤面包机等家用电器的控制和通信。
由于智能化家电的市场需求低于预期，Sun公司放弃了该项计划。随着1990年代互联网的兴起，Sun公司看到了Oak在互联网上应用的前景，改造了Oak，于1995年5月以Java的名称正式发布。



嵌入式->web->大数据->......

[基础语法没怎么变，主要是JVM的垃圾回收机制]

* 1991年，Sun公司的Green项目，James Gosling，Oak编程语言
* 1995年，推出Java测试版
* 1996年，JDK1.0
* 1997年，JDK1.1
* 1998年，JDK1.2，早期版本缺陷的大改动，革命性版本，更名为Java2
* 1999年，java分成 J2SE，J2EE，J2ME，JSP/Servlet技术诞生
* 2004年，J2SE 5.0（1.5.0）Tiger老虎，重要性版本，J2SE 1.5 更名为 J2SE 5.0
* 2006年，J2SE 6.0（1.6.0）Mustang野马，各版本更名。J2EE -> Java EE，J2SE -> Java SE，J2ME -> Java ME
* 2009年4月20日，甲骨文收购Sun公司，交易价达74亿美元
* 2011年，Java SE 7.0
* 2014年，Java SE 8.0
* 2017年，Java SE 9.0
* 2018年3月，Java SE 10.0
* 2018年9月，Java SE 11.0
* 2019年3月，Java SE 12.0

​		Java编程语言的风格十分接近C++语言。继承了C++语言的部分特性，同时优化了部分内容。太阳微系统对Java语言的解释是：“Java编程语言是个简单、面向对象、分布式、解释性、健壮、安全与系统无关、可移植、高性能、多线程和动态的语言”

| c++                      | java                                                        |
| ------------------------ | ----------------------------------------------------------- |
| 面向对象技术的核心       | 继承了“面向对象技术的核心”                                  |
| 指针                     | 用“引用”取代（指针易引起错误）                              |
| 运算符重载和多重继承特性 | 用“接口”取代                                                |
|                          | 增加垃圾回收功能                                            |
|                          | 引入了泛型编程、类型安全的枚举、不定长参数和自动装/拆箱特性 |



### 3.java技术体系

##### （1）技术体系

![java技术体系](otherSource\java技术体系.png)

**JDK(java development kid)与JRE(java running environment)的关系：**

JDK:支持Java程序开发的最小环境。JDK = Java程序设计语言+Java虚拟机+Java API类库。

JRE:支持Java程序运行的标准环境。JRE=Java虚拟机 +Java API类库中的Java SE API子集 。

##### （2）技术体系分支：J2EE，J2SE，J2ME

| J2EE (Java EE)                                               | J2SE(Java SE)                     | J2ME(Java ME)                       |
| ------------------------------------------------------------ | --------------------------------- | ----------------------------------- |
| Java 2 Enterprise Edition（企业版）                          | Java 2 Standard Edition（标准版） | Java 2 Micro Edition（微型版）      |
| 定位在服务器端应用/企业级领域                                | 定位在个人计算机应用/桌面应用领域 | 定位在消费性电子产品应用/嵌入式领域 |
| Java API组件+Web组件，消息组件，EJB组件，分布式组件，事务组件 | Java API组件                      | Java API组件+适应设备的特殊组件     |

##### （3）Java虚拟机（JVM: Java Virtual Machine）

![jvm](otherSource\jvm.png)

* JVM是一种用于计算机设备的规范，即虚拟的用于执行字节码文件的计算机。
* 是Java最核心的技术，也是跨平台的基础
* 可使用软件实现，IBM\SUN\BEA等；可使用硬件实现，sun\intel公司正在研发的java芯片



### 4.java技术优势

##### 跨平台性：

（硬件不同软件环境差异大）摆脱硬件平台的束缚。

  

![java文件编写到执行原理](otherSource\java文件编写到执行原理.png)



<font  color=#808080 size=1> <源文件： [java语言发展.drawio](otherSource\java语言发展.drawio) ></font>

字节码文件可以在具有java虚拟机的任何设备上运行。java虚拟机中的java解释器负责将字节码文件解释成特定的机器语言进行运行

Java：一次编译，到处运行；C：多次编译，到处运行

![image-20200419142819425](otherSource\c.png)

##### 安全性：

* 取消了指针（可移位运算指向不管该区域是否可用，容易数组越界）
* 提供了自动内存管理机制
* 字节码传输过程中使用公开密钥加密机制 （PKC）
* 运行环境提供四级安全性保障机制：字节码校验器-类装载器-运行时 内存布局-文件 访问限制

##### 完全面向对象的(oop)：

##### 健壮性：

强制类型机制 、异常处理、垃圾自动回收机制、安全检查机制



资料参考：
https://zh.wikipedia.org/wiki/Java
https://github.com/bjmashibing/java/blob/master/javase/ppt/01--%E5%88%9D%E8%AF%86java.pdf

https://blog.csdn.net/qq_39091292/article/details/84859611