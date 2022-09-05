![](image/c.png)

# C - 00 Manual

> 相信小伙伴已经看过日常基础部分辣，所以你应该有了一个 IDE （~~不会是C-free吧~~），和配置好的 GCC 编译环境。
>
> **C - 01 和 C - 02 我们希望在 Windows 环境下运行，C - 03 到 C - 05 我们更希望是在 Linux 环境下运行。**希望小伙伴们提前配置好相关环境。
> 该部分为后续试题的一些必要技术，按需拿取，可帮助你解题。


## Part 1 C programmer's manual （Linux）
当我们遇到了一个陌生函数或者头文件时，我们可以使用通过 Linux 终端查询相关函数使用方法信息。

1.  查询scanf函数的使用方法： 
```shell
~ > man scanf
```

2.  查询stdio.h标准库相关信息： 
```shell
~ > man stdio
```

## Part 2 Compile and run （Linux）
对于人么来说，C语言源代码是通俗易懂的，而对于冷冰冰的机器而言，源代码就是天书。为了使机器能够理解代码意图，我们得把他翻译成机器语言。
假设我们已经写好了一个源程序，命名为 `main.c`，我们在此目录下打开终端，键入以下命令：
```shell
~ > gcc -Og main.c -o main
```
此时目录下产生一个新的文件`main`，它就是**可执行目标文件**（executable object file），我们在终端键入以下命令：
```shell
~ > ./main
```
此时你的程序就跑起来辣。
上述例子是最简单的编译命令，当然这在后续题目中是远远不够的，比如，`main.c` 需要线程创建，此时，编译命令如下：
```shell
~ > gcc -Og main.c -o main -lpthread
```
该命令中，`-Og`，`-o`，`-lpthread`是 `GCC` 命令的编译参数，有关编译参数的更多内容，可参见网页：[gcc编译参数](https://www.runoob.com/w3cnote/gcc-parameter-detail.html)
所有程序都可以设置运行参数，假设有一个C语言可执行程序`main`：
```shell
./main -t /usr/bin/g++
```
通过`-t`选项，我们获得了`/usr/bin/g++`参数。
在C程序中如何获取对应参数，可以使用`getopt`函数处理，详细内容请查询`C programmer's manual`。

## Part 3 Input and Output (I/O)
在`stdio.h`库中，提供了以下输入函数。
```
scanf();    getchar();    gets();   fscanf();   fgets();  等等
```
在`stdio.h`库中， 提供了一下输出函数。
```
printf();   putchar();   puts();    fprintf();   等等
```
相关细节，请查询`stdio.h`标准库。
然而，这些函数可能是不安全的。比如gets()就存在安全漏洞，~~你可以通过~~~~gets()~~~~向程序注入你的攻击代码~~。这些stdio已经可以解决大部分的I/O问题，但是对于网络编程，出现的问题可能会使你摸不着头脑。所以有必要了解一下系统级I/O——read and write function。更多内容，可以阅读《CSAPP：3e》第10章。

## Part 4 学会Debug
> 程序设计时的初衷总是好的，但是代码运行结构总是出人意料的。`bug`总会时不时的找你麻烦。学会debug技巧，薄纱烦人的bug。

越高大上的IDE越有比较舒适的`debug`体验，例如`CLion`。越是普通的IDE，`debug`起来很是难受。
[CLion调试教程](https://www.jetbrains.com/zh-cn/clion/features/run-and-debug.html)
[vscode调试教程](https://baijiahao.baidu.com/s?id=1693398887373801447&wfr=spider&for=pc)
[Code::Blocks调试教程](http://c.biancheng.net/view/9452.html)
其他IDE的调试就显得不太友好。
（~~然而我们要学习一个最不友好的调试方式~~）

### gdb调试
> 什么是`gdb`？
> UNIX及UNIX-like下的调试工具。或许，各位比较喜欢那种图形界面方式的，像VC、BCB等IDE的调试，但如果你是在 UNIX平台下做软件，你会发现GDB这个调试工具相比于VC、z的优点是具有修复网络断点以及恢复链接等功能，比BCB的图形化调试器有更强大的功能。

当我们执行以下命令的时候，
```shell
~ > gcc -Og main.c -o main
```
会生成`main`（Linux）或者`main.exe`（Windows）的可执行文件
执行以下命令后
```shell
~ > gdb main
```
会进入gdb调试。使用gdb的help指令可以获得gdb的帮助文档

### 如何设定断点：
```
break main  \\在main函数入口设置断点
break * 0x123456  \\在地址0x123456处设置断点
delete 1 \\删除断点1
delete  \\删除所有断点
```
对`break * 0x123456`的理解：
输入以下命令：
```shell
~ > objdump -d main > main.d
```
此时会生成`mian.d`的汇编代码文件，打开他，你会发现形如以下的代码：
```
    10a4:	31 ed                	xor    %ebp,%ebp
    10a6:	49 89 d1             	mov    %rdx,%r9
    10a9:	5e                   	pop    %rsi
    10aa:	48 89 e2             	mov    %rsp,%rdx
```
每一行前面`10a4`等就是每一行指令的16位地址。
在gdb中输入`run`，开始运行程序，程序会自动达到你设定的断点位置。
gdb中输入`nexti`，执行下一步。
更多gdb操作，请参照群文件gdb参考文档。如果想要GUI界面，试试-tui的选项。

## **无需提交**
