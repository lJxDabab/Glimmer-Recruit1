![](image/daily.png)

# 日常-08 Python入门

> `难度系数`：简单
>  
> 现在这个卷到爆棚的时代，Python 网课满天飞，连小学都开 Python 课，出去可以说自己不会 C++，可以说自己不会Java，但是绝不能说自己不会 Python😎！
>  
> 不会吧不会吧不会还有人不会 Python 吧，其实现在学也不晚！
>  
> **”价值3W元Python课，冒死上传！！！”**
>  
> ![](https://zlkqzimg-1310374208.cos.ap-chengdu.myqcloud.com/image-20220715155705761.png#crop=0&crop=0&crop=1&crop=1&id=tSgOr&originHeight=267&originWidth=363&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
>  
> **”电子科技大学教授一周讲完的Python，学完立马就业！！！“**
>  
> ![](https://zlkqzimg-1310374208.cos.ap-chengdu.myqcloud.com/image-20220715155841266.png#crop=0&crop=0&crop=1&crop=1&id=iSE0I&originHeight=266&originWidth=345&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
>  
> **温馨提示：以上网课质量参差不齐，请谨慎选择**
> 初学者网课学习推荐小甲鱼的网课，书推荐图灵出版社的Python入门书
> 
> 打个小广告：大家一起学 Python，学完进军**机器学习**，成为一代算法大佬😀


## Python简介

Python 是一个高层次的结合了解释性、互动性和面向对象的脚本语言

### Python 是一种解释型语言

- 解释型语言，这意味着开发过程中没有了编译这个环节。类似于PHP和Perl语言
- 我们编写的**源代码（就是自己写的 print 等语句的集合）**是人类语言，我们自己能够轻松理解；但是对于计算机硬件（CPU），源代码就是天书，根本无法执行，计算机只能识别某些特定的**二进制指令（许多个 0 和 1 组成），在程序真正运行之前必须将源代码转换成二进制指令**。
- 所谓的二进制指令，也就是**机器码**，是 CPU 能够识别的硬件层面的“代码”，简陋的硬件（比如古老的单片机）只能使用几十个指令，强大的硬件（PC 和智能手机）能使用成百上千个指令。

然而，究竟在什么时候将源代码转换成二进制指令呢？不同的编程语言有不同的规定

1. **编译型语言：**有的编程语言要求必须**提前将所有源代码一次性转换成二进制指令**，也就是生成一个可执行程序（Windows 下的 `.exe`），**再执行该可执行程序**，比如 C 语言、C++、Golang、Pascal（Delphi）、汇编等，这种编程语言称为编译型语言，使用的转换工具称为编译器。
2. **解释型语言：**有的编程语言可以一边执行一边转换，需要哪些源代码就转换哪些源代码，**将一句源代码转化为机器指令后后立即执行该指令，再转换下一句**，不会生成可执行程序，比如 Python、JavaScript、PHP、Shell、MATLAB等，这种编程语言称为解释型语言，使用的转换工具称为解释器。

-  编译型语言一般是不能跨平台的，也就是不能在不同的操作系统之间随意切换，因为**转换为的可执行程序中的机器码是每个平台间独有的，而不是通用的**。但是解释型语言，**由于是只有源代码，要用的时候现用现转换**，所以是可以跨平台的 
-  但是**编译型语言的效率是远高于解释型语言的**（这个也很好理解嘛，别人编译型语言是原先翻译好的，解释型语言还要现翻译，快得上去才有鬼了🤡），所以计算机的一些底层功能，或者关键算法，一般都使用 C/C++ 这种编译型语言实现，只有在应用层面（比如网站开发、批处理、小工具等）才会使用解释型语言 
-  但是上述局限一定是绝对的吗，非也非也，程序语言得水太深，咱把握不住啊！比如Java是要进行编译的，但是可以进行跨平台运行，具体原理就不细嗦了。 

### Python 是交互式语言

-  这意味着，可以在命令行（shell）输入 `python`或 `ipython`或 `jupyter-notebook`进入交互式 Console 界面。
-  举个栗子🌰： 

我们现在要打印**“微光人均二刺螈, 南桐还多，嘎嘎香！”**，需要使用如下代码：

```python
a = "微光人均二刺螈"
b = ", 南桐还多，嘎嘎香！"
print(a + b)     # 本例是把a和b加起来一起打印
```

我们知道Python是解释型语言，所以本例会先翻译 `a = "微光人均二刺螈"`，再执行该语句，将 `a`赋值并存入内存。再翻译 `b = ", 南桐还多，嘎嘎香！"`，再执行，将b赋值并存入内存。再最后翻译 `print(a+b)`，再执行，打印句子。

相信你的代码习惯是把三句语句写完了，再一并按照上述进行运行。但是Python是解释型语言，意味着我们可以**先编写并运行一部分代码后，再在后续慢慢添加代码并运行**，而不用像编译型语言，要一次性将源代码编写完，下面展示使用交互式 console 编写上述语句（图中的ENTER表示在最后按一下回车）：

![](https://zlkqzimg-1310374208.cos.ap-chengdu.myqcloud.com/image-20220716001947803.png#crop=0&crop=0&crop=1&crop=1&id=mVfw7&originHeight=122&originWidth=432&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

步骤：先输入 `a = "微光人均二刺螈"`，再按回车执行，该语句执行并处理完后，才开始输入 `b = ", 南桐还多，嘎嘎香！"`，再按回车执行，执行完后才开始输入 `print(a+b)`，执行最后一句语句，并打印语句。

- 这意味着 Python 作为史上最好用的脚本语言，可以在你的任何工作路径下输入 `python`进入 console 界面，逐步编写并运行你的脚本
- 交互式最大的好处在于：当你的脚本处理比较复杂、持续时间较长时，比如脚本先对某个大文件执行时间长达一个小时的修改，然后进行保存。在以脚本方式运行时，如果在 50 min 时脚本运行出现了 bug，脚本将结束运行，脚本运行的中间结果将全部丢失，你又得再等 50 min，并且之后很可能还会有 bug；而在 console 的方式下，你可以将整个脚本逐句或逐个子任务执行，保证不会丢失全部的中间结果，并根据执行结果实时调整之后的代码
- jupyter notebook 是另一种交互式界面，它将代码与 Markdown 组合在一起，可以得到更加直观、优雅的体验：

![image.png](image\D8-1.png)

### Python 是面向对象语言（OOP）

- 这意味着 Python 支持面向对象的风格或代码封装在对象的编程技术，和 Java 一样，但是语法相对于Java更加自由，并没有 Java 近乎偏执的面向对象

## Python环境安装

- Windows系统上，建议先安装 Anaconda，再使用 Anaconda 进行 Python 环境的安装，Anaconda 可以更方便地安装和管理 Python 虚拟环境
- 安装好Anaconda后，建议学习一下 Anaconda 的基本指令，如：

```
conda create -n env_name python=3.7     --创建一个名字为env_name的python版本为3.7的虚拟环境
```

这样就可以直接创建一个指定版本的 Python 环境，**Python版本不是特别重要，建议还是使用最经典的v3.6或v3.7**。如果你对机器学习感兴趣，想要安装GPU版本的深度学习框架，那么一定要在官网搞清楚版本！

-  上述指令只是建立了一个纯纯只有 Python 解释器的基础环境，我们**还需要 **`**conda install**`**或 **`**pip install**`**命令（两者选其一即可）来安装自己需要的库**，如 numpy、tensorflow 等。给一个小 tip：**进行安装的时候一定要换源，将 conda 或者 pip 命令的下载地址，更改为国内的镜像源** 
-  那么到现在我们就完成了 Python 环境的安装，我们还需要一个 IDE，能更方便快捷地编程，推荐 pycharm、vs code等 

## 来个小Demo🙄

- 我们将使用 matplotlib 库，一个 Python 中常用的数据可视化库，来写一个小 Demo：

```python
# 微光工作室成立于2012年，为软件学院创新工坊最早的几大工作室之一
# 自成立以来，二刺螈浓度持续上升
# 画一个微光工作室2012年至2021年二刺螈浓度变化的折线图
import matplotlib.pyplot as plt

# 年份和二刺螈浓度，一一对应

# 生成横坐标：2012 - 2022 的年份
years = list(range(2012, 2022))

# 生成纵坐标：二刺螈浓度
concentration = [56, 64, 67, 83, 74, 71, 85, 88, 90, 93]

# 画图, x轴为年份, y轴为浓度
plt.plot(years, concentration)
plt.title("微光二刺螈浓度变化图")
plt.xlabel("年份")
plt.ylabel("浓度/%")
plt.show()
```

运行结果：

![](https://zlkqzimg-1310374208.cos.ap-chengdu.myqcloud.com/image-20220716010855141.png#crop=0&crop=0&crop=1&crop=1&height=360&id=rzcXp&originHeight=480&originWidth=640&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=&width=480)

## 本题提交方式

> 本题只是带大家初识Python，无需提交


## 出题者联系方式

QQ：1227609248

邮箱：[1227609248@qq.com](1227609248@qq.com)
