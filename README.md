# Kaldi Learning Notes
[深度学习之卷积和池化](https://www.cnblogs.com/believe-in-me/p/6645402.html)

1 卷积神经网络CNN由输入层、巻积层、激活函数、池化层、全连接层，input-conv-relu-pool-fc 

(1)卷积层：特征提取 

感受野的深度必须和输入图像的深度相同，通过filter与输入图像卷积得到一个特征，通常会设置多层卷积层来得到更深层次的特征。

**权值共享原则**

（2）池化层

对特征进行压缩，简化复杂度，提取主要特征

- Avy Pooling
- Max Pooling(主要)

（3）全连接层

连接所有特征，输出给分类器（如softmax函数）
