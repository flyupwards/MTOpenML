# 机器学习-55:支持向量机分类算法(Support Vector Machine)含代码

> [机器学习原理与实践(开源图书)-总目录](https://blog.csdn.net/shareviews/article/details/83030331)

支持向量机(Support Vector Machine)分类算法属于监督学习算法。常用分类算法包括：逻辑回归(Logistic Regression, LR)、K最近邻(k-Nearest Neighbor, KNN)、朴素贝叶斯模型(Naive Bayesian Model, NBM)、隐马尔科夫模型(Hidden Markov Model)、支持向量机(Support Vector Machine, SVM)、决策树(Decision Tree)、神经网络(Neural Network)和集成学习(ada-boost)。

> 告别碎片阅读，构成知识谱系。一起阅读和完善: [机器学习原理与实践(开源图书)](https://github.com/media-tm/MTOpenML)

在1963年，Vapnik使用支持向量机(Support Vector Machine)解决模式识别问题，关键样本被认为是支持向量。在1971年，将核技巧引入到支持向量机(Support Vector Machine)解决非线性问题。在1995年，Vapnik提出基于机(Support Vector Machine)的学习理论。支持向量机（support vector machines, SVM）是一种二分类模型，它的基本模型是定义在特征空间上的间隔最大的线性分类器，间隔最大使它有别于感知机，彻底解决了非线性、高维数、局部极小点等问题。支持向量机引入了核技巧，使其支持非线性分类器。

## 1 算法原理

支持向量机(Support Vector Machine)分类算法要求正确划分训练数据集并且几何间隔最大的分离超平面，并且要求几何间隔最大的分离超平面为划分类别的依据。超平面的间隔越大，分类的确信度(confidence)也越大。对于输入空间中的非线性分类问题，可以通过非线性变换将它转化为某个维特征空间中的线性分类问题，在高维特征空间中学习线性支持向量机。由于在线性支持向量机学习的对偶问题里，目标函数和分类决策函数都只涉及实例和实例之间的内积，所以不需要显式地指定非线性变换，而是用核函数替换当中的内积。

输入数据：线性可分/不可分的数据集(x1,y1),(x2,y2),...,(xm,ym)
输出结果：输出是分离超平面的参数w∗和b∗和分类决策函数。

支持向量机(Support Vector Machine)分类算法的核心步骤如下:

- 数据清洗：数据规范化, 了解数据的基本特征;
- 构造约束优化问题,使用最小二乘法构建优化函数
- 如果是线性不可分的数据集，通过核函数(Kernel)将数据映射到高维线性可分空间
- 分类超平面为：w∙x+b=0
- 分类决策函数为：f(x)=sign(w∙x+b)

支持向量机(Support Vector Machine)分类算法的核心优势如下：

- 计算伸缩性: 计算复杂度高，主流的算法是O(n^2)的，仅仅适合小样本学习问题;
- 参数依赖性: 可调节参数较少;
- 普适性能力: 泛化能力好，能解决高维问题；
- 抗噪音能力: 对缺失数据敏感，但是可以避免神经网络结构选择和局部极小点问题。
- 结果解释性: 结果解释有难度。

## 2 算法实例

[TODO, Coming Soon!]

## 3 典型应用

超参数降维和超参数分类，均可以使用支持向量机。

## 系列文章

- [深度学习原理与实践(开源图书)-总目录](https://blog.csdn.net/shareviews/article/details/83040730)
- [机器学习原理与实践(开源图书)-总目录](https://blog.csdn.net/shareviews/article/details/83030331)
- [Github: 机器学习&深度学习理论与实践(开源图书)](https://github.com/media-tm/MTOpenML)

## 参考资料

- [1] 周志华. 机器学习. 清华大学出版社. 2016.
- [2] [日]杉山将. 图解机器学习. 人民邮电出版社. 2015.
- [3] 佩德罗·多明戈斯. 终极算法-机器学习和人工智能如何重塑世界. 中信出版社. 2018.
- [4] 李航. 统计学习方法. 2012.
- [5] [支持向量机(SVM)——原理篇](https://zhuanlan.zhihu.com/p/31886934)
- [6] [理解SVM的三层境界](https://blog.csdn.net/v_july_v/article/details/7624837)