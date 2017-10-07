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

![biaos](

## 线性回归

为了使我们的住房范例更加有趣，我们可以考虑一个稍微更丰富的数据集

![sss](http://img.blog.csdn.net/20161111192340667)







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

对J(θ)进行求导:

![jjj](http://images.cnitblog.com/blog/492570/201409/082201316999035.png)

Thus, the value of θ that minimizes J(θ) is given in closed form by the equation：

![sss](http://images.cnitblog.com/blog/492570/201409/082210227775354.png)
















