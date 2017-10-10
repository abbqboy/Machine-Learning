# 欠拟合与过拟合

* 局部加权回归

* logistic 回归

* 感知器算法


## Logistic regression

我们可以忽略分类问题，忽略y是离散值的事实，并使用我们的旧线性回归算法尝试预测y给定x。

但是，很容易构造出这种方法执行得很差的例子。 直观地，当我们知道y∈{0,1}时，h（x）取大于1或小于0的值也没有意义。

为了解决这个问题，让我们改变我们的假设h（x）的形式。 我们会选择

![aaa](https://github.com/abbqboy/Sticker/blob/master/photo/logistic.jpg?raw=true)
