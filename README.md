# Kaldi Learning Notes

1 卷积神经网络CNN由输入层、巻积层、激活函数、池化层、全连接层，input-conv-relu-pool-fc 

[深度学习之卷积和池化](https://www.cnblogs.com/believe-in-me/p/6645402.html)

(1)卷积层：特征提取 

感受野的深度必须和输入图像的深度相同，通过filter与输入图像卷积得到一个特征，通常会设置多层卷积层来得到更深层次的特征。

**权值共享原则**

（2）池化层

对特征进行压缩，简化复杂度，提取主要特征

- Avy Pooling
- Max Pooling(主要)

（3）全连接层

连接所有特征，输出给分类器（如softmax函数）

2.kaldi语言识别 卷积神经网络

[kaldi学习笔记之卷积神经网络(CNN)](http://blog.csdn.net/DuishengChen/article/details/50085707)

（1）SpliceComponent

左右展开帧数 构成新的特征作为网络输入

（2）Convolution1dComponent

将输入特征转换为二维矩阵（类似于图像）进行卷积

（3）MaxpoolingComponent

降维和去除扰动

（4）NormalizeComponent

归一化

（5）AffineComponentPreconditionedOnline

全连接层的权重参数层，在Kaldi中，一层网络被拆成权重层和非线性变换层，权重层保存了网络的连接参数W，参数是可以修改的，而非线性变换层是固定的

（6）SoftmaxComponent

一旦定义后，非线性变换层就是固定的
