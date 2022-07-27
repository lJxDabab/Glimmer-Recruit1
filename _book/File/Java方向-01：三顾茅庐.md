![](https://cdn.nlark.com/yuque/0/2021/png/22004288/1625470150229-assets/web-upload/dd3150bc-fe04-4db3-b123-dd57612935f8.png#alt=img)

# Java方向-01：三顾茅庐

> `难度系数`：简单

> Java是一门非常实用且易学的语言，可以通过大量的在线教程，如菜鸟教程、b站视频等快速入门JavaSE（Java的基础部分）。

> 现在你已经是Java带师辣，快去切掉本题吧（


## 一顾茅庐

众所周知，YEWPO是工作室内数一数二的算法大手子和C语言出题人。tk_sky作为工作室蒟蒻，非常仰慕YEWPO的算法才能，想要向他拜师学艺。

然而出师未捷，YEWPO没有露面，只留下一句话：“就你这智商还配写C？”

tk_sky非常沮丧，到隔壁爪哇岛旅游散心。路上捡到一张神秘的纸条：

```java
public class HelloJava { public static void main(String[] args){ System.out.println("                               \n" + "                               \n" + "      ....            ....     \n" + "    .,@@/...,]@@@@]`...\\@@..   \n" + "   ./@/../@@@@@@@@@@@@\\..\\@\\.  \n" + "  ./@^.,@@@/`......,\\@@@`.=@\\. \n" + " .=@^.=@@@..        ..@@@^.=@^.\n" + " .@@..@@@`.          .,@@@..@@.\n" + " .@@..@@@.            .@@@..@@.\n" + " .\\@`.@@@^.          .=@@@.,@/.\n" + " .,@\\.,@@@`.        .=@@@`.@@`.\n" + "  .=@\\./@/..        ..\\@\\./@^. \n" + "   .,@@/.../]......]\\...\\@@`.  \n" + "     .....\\@@@@@@@@@@/.....    \n" + "           ...[[[[...           \n"+ "        Glimmer Studio         ");}}
```

纸条上密密麻麻，tk_sky只看懂了四个字母“Java"。可是他智商有限，搞不明白这张天书有何寓意。请聪明的你帮他揭示纸条的真面目吧！

### Task 1.

复制这段天书，在本地创建一个空文件"HelloJava.java"（不要更改文件名！），使用文本编辑器（记事本/vim等）编辑它，粘贴这段天书，然后通过命令行，使用Java编译并运行这段天书，看看结果如何！

> 回答要求：

> 1. 记录你完成本题的整个过程和遇到的问题，配以必要的截图等。
> 2. 说说你编译的过程中使用了什么命令，产生了哪些文件，这些命令和文件分别有什么作用。
> 3. 查找资料并结合本题，为什么说java`是，但不完全是`编译型语言？它和纯解释型语言（如python）、纯编译型语言（如C）有什么区别和相似之处？


#### Tips：

1. 
安装jdk

要进行Java开发，首先必须安装jdk（Java开发者工具包）。在后面的链接你可以下载到对应你系统的jdk：[https://www.oracle.com/java/technologies/downloads/](https://www.oracle.com/java/technologies/downloads/)

2. 
配置环境变量

以windows为例，安装jdk后，使用win+r键打开“运行”，输入"cmd"打开命令行，输入"java"后回车，可能出现“java不是内部或外部命令，也不是可运行的程序”之类的报错。这时需要配置环境变量才能直接使用"java"调用java。

建议参考网络教程：[Windows 10 配置Java 环境变量 | 菜鸟教程 (runoob.com)](https://www.runoob.com/w3cnote/windows10-java-setup.html)

3. 
编译和运行

配置完成环境变量后，在命令行使用"javac HelloJava.java" 编译程序，再使用"java HelloJava"运行程序。

什么？你问啥是命令行？[http://b.iou.ink/?q=5LuA5LmI5piv5ZG95Luk6KGM](http://b.iou.ink/?q=5LuA5LmI5piv5ZG95Luk6KGM)


## 二顾茅庐

在你的帮助下破解了天书的tk_sky非常高兴，带着破解好的纸条再次找到了YEWPO。看了看tk_sky电脑上的记事本软件，YEWPO冷哼一声，“就你这破记事本就想写程序啊？”  然后不屑的离去，留下帅气的背影。

tk_sky闻言备受打击，一蹶不振。你能教会他安装一个高端大气上档次的Java IDE（集成开发环境）吗？

### Task 2.

安装 IntelliJ IDEA（推荐） 或 Eclipse，使用它新建java项目并运行Task1的天书代码。

> 回答要求：

> 记录你完成本题的整个过程和遇到的问题，配以必要的截图等。


#### Tips:

IDEA有免费的社区版和付费的专业版。你电学生也可以去jetbrain官网提交学信网学籍报告拿到study licence。Eclipse是免费的。

## 三顾茅庐

在你的帮助下安好了IDE的tk_sky再次屁颠屁颠地去找YEWPO了。此时YEWPO正坐在工作室的4k显示屏前奋键盘疾敲，因为他正要[AK](https://baike.baidu.com/item/AK/18224776) 一场[AtCoder](https://atcoder.jp/)比赛。

由于要集中精神AK比赛，YEWPO不想被tk_sky打扰。于是甩给tk_sky一句话：“你但凡把这最简单的A题写出来，我就同意你。”

tk_sky看了看A题，瞬间就绝望了。请你帮助他把这道题做出来吧！由于tk_sky不会C语言，请你用Java完成本题。

### Task 3.

学习Java的基础语法，使用Java，编写代码完成[AtCoder Beginner Contest 252 A题](https://atcoder.jp/contests/abc252/tasks/abc252_a)。

> 简要题意：

> 输入一个整数N，输出ASCII码为N的字符。


> 回答要求：

> 将你的代码附在题解上。


#### Tips:

1. 本任务意在让你动手敲一敲Java代码，学习一下Java的数据类型和输入输出。上面的题目非常简单，和算法没什么关系。
2. 不知道什么是ASCII码？[http://b.iou.ink/?q=5LuA5LmI5pivQVNDSUnnoIE=](http://b.iou.ink/?q=5LuA5LmI5pivQVNDSUnnoIE=)
3. 对Java基础语法有疑惑？[Java 基础语法 | 菜鸟教程 (runoob.com)](https://www.runoob.com/java/java-basic-syntax.html)
4. 如果你感兴趣，可以注册一个atcoder账户提交你的代码试试

### 卑微的尾声

“YEWPO爷爷带我写算法吧！我已经完全学会Java了！”tk_sky哀求道。YEWPO刚AK完比赛，心情大好，于是欣然接受。还没等tk_sky开始庆祝，YEWPO接到了acm校队的电话，“哦，校队不招Java选手啊，那没事了。那个谁，你爬吧”。

于是tk_sky长达几个小时的算法竞赛生涯正式结束。完结撒花！

---

### 需要掌握的知识点

- jdk的安装
- java程序的编译/运行
- 安装IDE
- 简单的Java语法

### Tip

- 善用搜索引擎

### 本题提交方式

> 收件邮箱：glimmer401[@outlook.com ](/outlook.com ) 

> 主题格式： 学号-姓名-考核-Java-01

> 主题示例：2022090101012-张三-考核-Java-01


### 出题者联系方式

> tk_sky

> QQ：2071594767

> 邮箱：linhanyuan_km[@163.com ](/163.com ) 

