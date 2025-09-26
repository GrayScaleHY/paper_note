### 人脸识别

#### 一、L-softmax
Large-Margin Softmax Loss for Convolutional Neural Networks.pdf  
在本文中，我们提出了一个广义的大边际软最大损失（L-Softmax），它明确地鼓励了学习特征之间的类内紧性和类间可分离性。此外，L-Softmax不仅可以调整所需的裕度，还可以避免过拟合。我们还证明了L-Softmax损失可以通过典型的随机梯度下降来优化。 
1. 我们的关键直觉是样本和参数之间的可分性可以分解为具有余弦相似度的振幅和角的可分性，因此，本文的目的是将softmax损失推广到更一般的大边际softmax（L-Softmax）在角度相似性方面的损失，导致学习特征之间潜在的更大的角度可分性。




