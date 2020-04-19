# java开发准备 / Hello World / 编程风格

### 一 、java开发准备 

##### 1.安装JDK 搭建环境

- 下载 jdk-12.0.1免安装版本：https://www.oracle.com/java/technologies/javase-downloads.html

- 生成 jre：jdk目录下，管理员身份启用cmd，bin\jlink.exe --module-path jmods --add-modules java.desktop --output jre

- 环境变量配置：

  多版本切换 ，更改 JAVA_HOME  路径即可。

| 变量名    | 变量值                               |
| --------- | ------------------------------------ |
| JAVA_HOME | C:\Program Files\Java\jdk-12.0.1     |
| Path      | %JAVA_HOME%\bin;%JAVA_HOME%\jre\bin; |

- 检查是否搭建成功：重启cmd，java -version
- 其他补充说明：
  - 运行框：win+r打开，可根据输入的名称，打开相应的程序、文件夹、文档等
  - 命令行窗口 ：运行框中输入cmd
  - 环境变量：是操作系统中一个具有特定名字的对象，包含多个应用程序所将使用到的信息。在windows环境中的Path变量，当要求系统运行一个程序而未告知完整路径时，系统除了在当前目录下寻找还会到path中指定的路径中找。用户通过设置环境变量 ，更好的运行程序。（Path：系统指定可执行文件的搜索路径）

##### 2.安装开发工具  

- 文本编辑器：notepad++ (https://notepad-plus-plus.org/downloads/)
- 集成开发环境（IDE）：IntelliJ IDEA (https://www.jetbrains.com/idea/)
- 反编译工具：jd-gui.exe (http://java-decompiler.github.io/)

##### 3.准备 JDK 帮助文档

是jdk语言的完整说明，提供了 java中各种技术的详细资料，各种类的帮助说明。

https://docs.oracle.com/en/java/javase/12/

##### 4.掌握简单DOS命令

![image-20200419194045384](otherSource\常用dos命令.png)

### 二、Hello World

##### 1.代码编写

文本编辑器中如下编辑，保存为HelloWorld.java

```java
public class HelloWorld{
    public static void main(String[] args){
        System.out.println("Hello World !");
    }
}
```

##### 2.编译阶段

打开cmd，进入java文件所在目录，输入命令：javac HelloWorld.java，可以看到目录下多了个HelloWorld.class文件（编译的是文件 ，所以要加.java）

##### 3.执行阶段

打开cmd，进入java文件所在目录，输入命令：java HelloWorld，可以看到输出 Hello World !（运行的是类而不是class文件，所以不加.class）

##### 4.常见报错与原因

- java文件的名称必须跟public class名称保持一直
- 一个java文件中可以包含多个class，但是public class只能有1个
- public static void main (Sting[] args)是所有java程序的入口，想执行对应的java代码 ，必须添加该方法，且格式固定
- main方法中参数列表可以支持多种写法：String[] args,String []args,String args[]
- mian方法中参数名称一般为args，也可以是别的
- java代码编写每行结尾都需要以;结束
- java代码的代码块需要用{}括起来，且前后匹配

| 序号 | 错误                                                      | 原因                                                         |
| ---- | --------------------------------------------------------- | ------------------------------------------------------------ |
| 1    | ![报错-没有编译](otherSource\报错-没有编译.png)           | 执行Hello World，报错提示如下，原因是：没有编译就执行，即 ，没有生成class文件 |
| 2    | ![报错-编译非文件](otherSource\报错-编译非文件.png)       | 编译Hello World，报错提示如下，原因是：编译的是文件，要文件名全称包括后缀，这里缺少.java |
| 3    | ![报错-编译-目录错误](otherSource\报错-编译-目录错误.png) | 编译Hello World，报错提示如下，原因是：没在文件目录下去编译。 |
| 4    | ![报错-执行-乱码](otherSource\报错-执行-乱码.png)         | 执行Hello World，报错提示如下，原因是 ：命令行窗口默认编码模式是GBK，而我们编辑的java文件默认保存格式是UTF-8。解决方案 |

执行后乱码问题解决方法：

（1）修改命令行的编码格式：输入chcp 65001，再重新编译和运行

[chcp说明：全称-Changes the active console code page；功能-显示或这只活动代码页编号；常用码-“chcp 65001” UTF-8代码页，“chcp 936 ”默认的GBK，“chcp 437 ”美国英语 ]

（2）修改java文件的编码格式

* 记事本：另存为，修改编码为ANSI
* notepad++：Encoding ->Encode  in ANSI

### 三、java编程风格

[《阿里巴巴JAVA开发手册》]: https://edu.aliyun.com/course/417/lesson/list?spm=5176.8764728.aliyun-edu-course-tab.2.f76252bbz8oK0a

##### 1.代码缩进

##### 2.成对编程

##### 3.见名知意

##### 4.注释

为程序写的说明提高可读性。注释不会出现在字节码文件中（编译时会跳过注释语句）

* 单行注释 //
* 多行注释 /* */
* 文档注释 /** */，可通过JDK提供的Javadoc命令 ，生成程序的API文档
