![](image/c.png)
# C - 03 B * C by A
> 难度系数：一般-困难
>
> C是一门最接近的底层的语言，了解并掌握一些底层汇编是必要，有助于提升你的能力。
>
> C - 03 之后，请使用`Linux`环境！


## Part 1 Assembly in C
众所周知，tk_sky是工作室的算法大手子。他的算法这么厉害，让队友YEWPO非常羡慕。YEWPO认为tk_sky一定有什么学习算法的终极奥秘隐藏在他的电脑里。于是YEWPO使用物理办法黑入了YEWPO的电脑，发现了一串他从来没见过的神秘代码:

### Task 1

```c
#include <stdio.h>

int function(int a, int b, int c) {
    int res = 0;
    __asm__ __volatile__("mov %%rcx, %%rdx \n\t"
                         "add %%rbx, %%rdx \n\t"
                         "add %%rdx, %%rax \n\t"
            :"=a"(res)
            :"a"(a), "b"(b), "c"(-c)
            :"%rdx");
    return res;
}

int main() {
    int x, y, z;
    scanf("%d%d%d", &x, &y, &z);
    printf("%d\n", function(x, y, z));
    return 0;
}
```

阅读以上程序，回答下列问题：

1. `function`函数的功能是什么？试着分析一下这个函数。
2. `volatile`起到什么样的作用？
3. `mov`,`add`起到什么样的效果？
4. `rcx`,`rdx`,`rbx`代表着什么？
5. 写出内联汇编的格式要求。

#### tips

- 汇编语言的基础语法
- 寄存器的符号表示
- 内联汇编语法

### Task 2

YEWPO终于明白上述代码的意思，在暗示下，YEWPO找到tk_sky曾经的笔记：
~~显而易见，加法是一类非常简单的运算~~，所以计算机在计算加法和减法（减法也是加法）时只需要1个时钟周期；~~然而，乘法和除法是一类非常难的计算~~（这怎么会难呢，不是很简单吗），所以计算一次乘法，需要3个时钟周期，计算一次除法，需要3 ~ 30个时钟周期，远远慢于加法运算。对计算机而言，位运算是它最喜欢的运算，~~然而出题人却很不喜欢，这不比乘法运算难？~~所以位运算计算时间和加法相当。
综上所述，我们要避免使用乘法和除法运算。（~~用循环写乘法和除法~~）即：

![](image/f2deae536f264f3e1ea030263e52ac24.svg)

请以最优的方法实现下列计算：

#### Description
给定一个整数`x`，计算`15x`。
#### Sample input
```
3
```
#### Sample output
```
45
```
#### Request
请以你认为的最优的计算方法用内联汇编实现。
#### tips

- 15有什么特点
- 避免使用乘法
- 位运算

## Part 2 Disassemble（选做）
经过一番寻找，YEWPO竟然真的发现了一个"secret"！然而要打开这个文件，需要输入密码。这时tk_sky已经结束集训回来了，为了以后能继续抱他的大腿，YEWPO只好迅速拷贝了程序离开了tk_sky的电脑。

### Task 3

心有不甘的YEWPO找到了你，希望你能想办法破解密码以破解算法的终极奥秘！
获得程序方式：
```shell
linux > wget https://github.com/YEWPO/secret/raw/main/secret
```
如遇权限问题，请根据情况使用以下命令：
```shell
chmod 777 secert
```
#### tips

- 找到源码
- ASCII
- 反汇编
- GDB
- IDA？？

## 题目要求

- 正确的可执行的代码
- 回答题目中的问题时，表达自己的想法
- 程序设计分析
- 代码运行的截图
## 本题提交方式

> 收件邮箱：glimmer401@outlook.com  
>
> 主题格式： 学号-姓名-考核-C-03
>
> 主题示例：2022090101012-张三-考核-C-03

## 出题人联系方式
> QQ：2398696309
>
> 邮箱：2398696309@qq.com 

