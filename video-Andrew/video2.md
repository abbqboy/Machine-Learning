# 吴恩达机器学习第二课学习笔记

监督学习应用：梯度下降

* 线性回归

* 梯度下降

* 正规方程组

## 房价预测

Suppose we have a dataset giving the living areas and prices of 47 houses from Portland, Oregon:

![ssss](https://github.com/abbqboy/Sticker/blob/master/photo/%E6%88%BF%E4%BB%B7%E5%8D%95%E5%9B%A0%E7%B4%A0.jpg?raw=true)

我们可以绘制这些数据：

![sssss](https://github.com/abbqboy/Sticker/blob/master/photo/%E6%88%BF%E9%97%B4%E5%8D%95%E5%9B%A0%E7%B4%A0%E7%BB%98%E5%88%B6.png?raw=true)

m = #training examples

x = 输入变量

y = 输出变量

我们可以将监督学习的整个过程用下图表示：

![biaos](https://github.com/abbqboy/Sticker/blob/master/photo/%E7%9B%91%E7%9D%A3%E5%AD%A6%E4%B9%A0%E8%BF%87%E7%A8%8B.png?raw=true)

## 线性回归






## LMS algorithm

我们要选择θ以便最小化J（θ）。 

为了做到这一点，我们可以使用从θ的一些“初始猜测”开始的搜索算法，并且重复地改变θ使得J（θ）更小，直到希望我们收敛到最小化J（θ）的θ值。 

具体来说，我们考虑梯度下降算法，它以一些初始θ开始，并重复执行更新：

![aaa](http://img.blog.csdn.net/20160724132622397)

（对于j = 0，...，n。的所有值，同时执行此更新）

这里，α称为学习率。 这是一个非常自然的算法，它反复地沿着J.最快下降的方向迈出一步。

为了实现这个算法，我们必须找出右边的偏导数项。 如果我们只有一个训练样本（x，y），我们可以忽略J.的定义中的总和，我们首先处理它。我们有：

![qqqq](http://img.blog.csdn.net/20160724132712507)


为了使我们的住房范例更加有趣，我们可以考虑一个稍微更丰富的数据集

![sss](http://img.blog.csdn.net/20161111192340667)

(关键在这一步，我猜，作者是默认对其求导的时候，就把其看作一个累加值，y也是累加值，这样求出来的似乎是一样的（求导后是一样的，未求导前不一样，注意平方和与和的平方的差别） 

![qqq](http://img.blog.csdn.net/20160724132740133)

批梯度下降算法，每一次迭代都要用所有的数据。当训练数据非常大时，这个方法有些不适用。 

这个时候用随机梯度下降算法：

![aaa](http://img.blog.csdn.net/20160724132815237)

每一次都用上次的样本开始进行迭代。

在这个算法中，我们反复运行训练集，每次遇到训练样例时，我们只会根据错误的梯度来更新参数。

而批量梯度下降必须在进行一个步骤之前扫描整个训练集,使得运算量十分大。

通常，随机梯度下降使得“最接近”的最小比批量梯度下降快得多。 

注意，它可能永远不会“收敛”到最小值，并且参数θ将保持围绕J（θ）的最小值振荡;但实际上，接近最小值的大多数值将与真实最小值相当好的近似值。 

由于这些原因，特别是当训练集较大时，随着梯度梯度下降，随机梯度下降通常是优选的。


## 正规方程组

梯度下降给出了一种求minimizing J的方法。

下面我们讨论第二种方法，而不使用迭代算法。 

### Matrix derivatives(矩阵的求导)

首先定义![ww](http://images.cnitblog.com/blog/492570/201409/082123225904638.png)表示m×n的矩阵，那么对该矩阵进行求导可以用下式表示，可以看出求导后的矩阵仍然为m×n

![qqq](http://images.cnitblog.com/blog/492570/201409/082124567468939.png)

这里要用到矩阵迹的特性，trace. 对于一个n阶的方阵（n×n）,它的迹(tr)为对角线元素之和：

![qqqq](http://images.cnitblog.com/blog/492570/201409/082133141846068.png)

和其他的一些公式，证明省略。
tr AB = tr BA

![qqq](http://img.blog.csdn.net/20160724133045543)
![rrr](http://img.blog.csdn.net/20160724133056731)





假设训练样本：

![sss](http://images.cnitblog.com/blog/492570/201409/082153133405821.png)

y包含m维向量训练集：

![yyy](http://images.cnitblog.com/blog/492570/201409/082154109653649.png)

因为![ss](http://images.cnitblog.com/blog/492570/201409/082156509024886.png)所以：

![sssss](http://images.cnitblog.com/blog/492570/201409/082157219655764.png)

又因为![qqqq](http://images.cnitblog.com/blog/492570/201409/082158401999562.png)，根据最小二乘规则，代价函数可以写成：

![qqqq](http://images.cnitblog.com/blog/492570/201409/082159422468873.png)

对J(θ)进行求导:

![jjj](http://images.cnitblog.com/blog/492570/201409/082201316999035.png)

Thus, the value of θ that minimizes J(θ) is given in closed form by the equation：

当导数=0

![ppp](http://images.cnitblog.com/blog/492570/201409/082210227775354.png)
![sss](http://images.cnitblog.com/blog/492570/201409/082210380596985.png)
















