# 欠拟合与过拟合

* 局部加权回归

* logistic 回归

* 感知器算法


## Logistic regression

我们可以忽略分类问题，忽略y是离散值的事实，并使用我们的旧线性回归算法尝试预测y给定x。

但是，很容易构造出这种方法执行得很差的例子。 直观地，当我们知道y∈{0,1}时，h（x）取大于1或小于0的值也没有意义。

为了解决这个问题，让我们改变我们的假设h（x）的形式。 我们会选择

![aaa](https://github.com/abbqboy/Sticker/blob/master/photo/logistic.jpg?raw=true)

称为逻辑函数或Sigmoid函数。



## 解读：感知器学习算法

我们现在稍微讨论一些具有一定历史意义的算法，当我们谈论学习理论时，我们也会回到以后。 

考虑修改逻辑回归方法以“强制”它输出0或1或完全相同的值。 为此，将g的定义改为阈值函数似乎是很自然的：

![aaa](https://github.com/abbqboy/Sticker/blob/master/photo/%E6%84%9F%E7%9F%A5%E5%99%A8.png?raw=true)

