![](https://cdn.nlark.com/yuque/0/2021/png/21738773/1625662437423-575c4356-71f3-4a57-a4ff-b6cea317655e.png#id=BcGYe&originHeight=300&originWidth=748&originalType=binary&ratio=1&status=done&style=none#crop=0&crop=0&crop=1&crop=1&id=LE1GJ&originHeight=300&originWidth=748&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

# 机器学习方向-05：BERT（面试直通车）

> `难度系数`：**出题人放飞自我的难度**🤮
>  
> **此题不建议新手尝试（即使你已经完成了前四题）。有机器学习基础的同学完成此题将直接获得机器学习方向面试资格，面试中我们会对你的这篇回答进行详细的提问，确保你的答案并非不经思考直接抄袭的内容。当确认你的答案真实有效后，可以直接加入微光工作室机器学习组。**
>  
> BERT是时下NLP最火且最常用的模型，是一种通过**在预训练时使用无监督**方法能在**每一层**实现**双向**表征的语言模型，并且使用微调的方法，在**具体的下游任务时不需要task-specific architecture**，只需要添加一两层和少部分参数，十分易于迁移
> 
> 如果是有很好的深度学习基础的同学， 还未接触过Transformer和BERT，我们建议阅读：
> Transformer：[https://proceedings.neurips.cc/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf](https://proceedings.neurips.cc/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf)
> BERT:[https://arxiv.org/pdf/1810.04805.pdf](https://arxiv.org/pdf/1810.04805.pdf)


## 前置知识

1. Word Embedding
2. RNN
3. LSTM模型结构
4. seq2seq模型
5. Transformer模型结构
6. 注意力机制
7. Pre-training和Fine-tuning
8. BERT模型结构

## 题目要求

1.  BERT是脱胎于Transformer模型的，Transformer中的重中之重就是其中的自注意力机制 （self-attention），**请介绍注意力机制，以及其优点（和RNN对比一下）。注意力机制还可以拓展为多头注意力机制，请简要介绍**。 
2.  请**介绍Transformer的结构**，Encoder和Decoder分开介绍。 
3.  请**介绍BERT的结构**，以及BERT的输入是如何构成的，**BERT的输入又和Transformer的输入有什么相同点和不同点**？ 
4.  请介绍BERT中的**Pre-training和Fine-tuning**是如何实现的（其中请重点回答Pre-training中的mask策略，以及为什么要这么设计）？ 

## 回答要求

1. 分点作答，必要时使用插图；
2. 不允许从任何地方抄原文过来。
3. 如果涉及到公式部分，建议稍稍学习一下Latex语法，在markdown中可以内嵌使用

## 本题提交方式

> 收件邮箱：glimmer401[@outlook.com ](/outlook.com ) 
主题格式：学号-姓名-考核-机器学习-05
主题示例：2020091202014-张三-考核-机器学习-05


## 出题者联系方式

QQ：1227609248

邮箱：[1227609248@qq.com](1227609248@qq.com)
