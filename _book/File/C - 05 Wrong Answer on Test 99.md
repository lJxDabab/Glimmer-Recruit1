![](image/c.png)
# C - 05 Wrong Answer on Test 99
> 难度系数：困难
> 
> 电子科技大学信息与软件工程学院有一套在线测评系统`icoding.run`（~~icopying~~），将陪伴你大学的第一年。
> 
> 在线测评（Online Judge）系统（简称OJ）是一个在线的判题系统。用户可以在线提交程序多种程序（如C、C++、Pascal）源代码，系统对源代码进行编译和执行，并通过预先设计的测试数据来检验程序源代码的正确性。
> 
> **在本题，我们将带你用C语言实现一个简单的OJ。难度较大，你可以在任何一个阶段提交你的解题报告。**


## Part 1 Socket
首先，你得发送你的代码吧。如何向系统（服务端）发送信息是我们要解决的第一个问题。

### Task 1

请编写一对C程序，实现你（客户端）向系统（服务端）发送一段代码，系统（服务端）打印出这段代码。返回给客户端提交成功信息。

#### challenges

- 如何处理运行参数
- 如何读取文件
- 进程间如何通讯，谈谈你对TCP和UDP的理解。
- 如何完整地发送和接受数据
- 如何跨局域网运行（当然你也可以在同一局域网运行）


**tips**

- `getopt`函数
- `I/O`
- socket编程
- 善用搜索

**client example**
```shell
linux > ./client -t <programFileAddress> -s <serverAddress> -p <serverPort>
```

```shell
linux > ./client -t example.c -s localhost -p 8081 
summit example.c success!
```

**server example**
```shell
linux > ./server -p <listenPort>
```

```shell
linux > ./server -p 8081
receiving...
#include <stdio.h>

int main() {
	return 0;
}
receive program file success!
```

## Part 2 Exe
现在系统（服务端）可以收到你的代码辣。为了方便我们后续操作，我们将收到的代码储存在系统（服务端）工作目录里。接下来，系统（服务端）就要尝试编译运行你的代码，并检查你的答案。
### Task 2
#### step 1
在系统（服务端）编写一个功能，如果编译成功，向用户返回编译成功的信息。如果编译失败，返回编译信息。
#### step 2
如果编译通过，我们就要检查代码运行结果是否正确了。尝试写一个代码答案检测程序，实现对**C - 01 task 1**的检测。并在该系统（服务端）调用你的检测程序并把得到测评结果反馈给用户。
请实现上述功能。
#### chanllenges

- 如何在发送数据和接受数据两个状态之间转化
- 如何在进程中加载其他进程
- 如何获取其他进程的输出流或者是错误流。
- 如何检查测评提交的代码
**tips**

- 设立状态TAG？
- fork/execve
- `I/O`重定向
**client example 1**

```shell
linux > ./client -t example.c -s localhost -p 8081
submitting...
submitted success!
compiling...
compile error!
 In function ‘main’:
/program/rec/main.c:4:26: error: ‘a’ undeclared (first use in this function)
    4 |   printf("hello, world", a);
      |                          ^
/program/rec/main.c:4:26: note: each undeclared identifier is reported only once for each function it appears in
```

**server example 1**

```shell
linux > ./server -p 8081
receiving...
received success!
compiling...
compile error!
```

**client example 2**

```shell
linux > ./client -t example.c -s localhost -p 8081
submitting...
submitted success!
compiling...
compile success!
running...
correct!(or Wrong Answer on Test %!)
```

**server example 2**

```shell
linux > ./server -p 8081
receiving...
received success!
compiling...
compile success!
running...
correct!(or Wrong answer!)
Test finished!
```

## Part 3 Concurrent
到这里，恭喜你基本实现了一个OJ系统辣！！！但是这个系统（C/S）只能一对一服务。然而，一对一的服务效率太低了，不能胜任现在网络服务需求。~~icoding可是可以同时处理多个代码的。~~
### task 3
完善程序，使服务端可以处理多个用户的请求。
**tips**

- methods
   - Part 2 fork的作用
   - I/O多路复用
   - 多线程
- 什么是线程，什么是进程，谈谈你的理解。

## 题目要求

- 正确的可执行的代码
- 描述自己遇到的问题，以及解决方法和解决结果
- 回答题目中的问题时，表达自己的想法，可以附图片
- 良好的代码习惯
- 从功能、性能、安全、稳定等角度不断完善你的程序（使之成为真正的OJ吧）（加分项）
- 代码运行的截图


## 本题提交方式
> 收件邮箱：glimmer401@outlook.com  
> 
> 主题格式： 学号-姓名-考核-C-05
> 
> 主题示例：2022090101012-张三-考核-C-05

## 出题人联系方式
> QQ：2398696309
> 
> 邮箱：2398696309@qq.com  

