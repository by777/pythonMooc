# Python机器学习应用

## 无监督学习

利用无标签的数据学习数据的分布或数据与数据之间的关系称作无监督学习。

+ 无监督学习与有监督学习的最大区别在于数据是否有标签
+ 无监督学习最常用的场景是聚类（clustering）和降维（dimension reduction）

### 聚类（Clustering）

聚类就是利用数据的相似性把数据分为多类的过程。评估两个不同样本的相似性，最常使用的方法就是计算两个样本之间的“距离”。

###### 欧氏距离：欧氏空间两点的直线距离

$$
d = \sqrt{\sum_{k=1}^{n} (x_{1k} - x_{2k})^2}
$$

###### 曼哈顿距离：又称为城市街区距离

$$
d = \sum_{k=1}^{n} |x_{1k} - x_{2k}|
$$

###### 马氏距离：数据的协方差距离，与尺度无关

###### 夹角余弦：余弦值越接近于1说明两个向量夹角越接近于0，越相似

###  降维(Dimension Reduction)

降维，就是在保证数据所具有的代表性特性或者分布的情况下，将高维数据转化为低维。

+ 数据的可视化

+ 精简数据

  ## 监督学习

  利用一组带有标签的数据，学习从输入到输出的映射，然后将这种映射关系应用到未知数据上，达到分类或回归的目的。

  + 分类：当输出是离散的，学习任务为分类任务
  + 回归：当输出是连续的，学习任务为回归任务

训练集 / 测试集的划分方法：7：3

### 分类学习

##### 评价标准

`精确率`：精确率是针对我们预测结果而言的，（以二分类为例）它表示的是预测为正的样本中有多少是真央的样本。那么预测为正就有两种可能了，一种就是把正类预测为正类（TP），另一种就是把负类预测为正类（FP），也就是
$$
P = {TP \over {TP + FP}}
$$
`召回率`：是针对我们原来的样本而言的，它表示样本中正例有多少被正确预测了。那也有两种可能，一种是把原来的正类预测为正类（TP），另一种就是把原来的正类预测为负类（FN），也就是
$$
P = {TP \over {TP + FN}}
$$

##### sklearn提供的分类函数

+ knn

+ naivebayes

+ svm

+ decision tree

+ neural networks等

  ### 回归分析

  回归：统计学分析数据的方法，目的在于了解两个或多个变量之间是否相关、研究其相关方向与强度，并建立数学模型。回归分析可以帮助人们在了解自变量变化时因变量的变化量。一般来说，通过回归分析我们可以由给出的自变量估计因变量的条件期许。

  ##### sklearn提供的回归函数

  Sklearn提供的回归函数主要被封装在两个子模块中，分别是：

  sklearn.linear.model和sklearn.processing

  + 普通线性回归函数（Linear Regression）
  + 岭回归（Ridge）
  + Lasso
  + 非线性回归函数，如多项式回归（PolynomialFeatures）则通过sklearn.preprocessing子模块调用

  

  