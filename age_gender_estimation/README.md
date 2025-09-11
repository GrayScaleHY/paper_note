#### 年龄-性别估计

##### 一、C3AE
C3AE: Exploring the Limits of Compact Model for Age Estimation  
code: [https://github.com/StevenBanama/C3AE](https://github.com/StevenBanama/C3AE)  
1. 对于小尺寸输入图片， 标准卷积要优于深度可分离卷积。  
2. 年龄两点表示法, 如下图所示，年龄由相邻两个年龄范围加权求得。  
![图片](images/年龄两点表示法.png)  
3. 联合训练,在特征层和回归层之间插入语义全连接层，定义两个loss， KL loss和MAE loss  
![图片](images/联合训练.png)  
KL loss测量真实值标签与预测年龄分布之间的差异，采用kl -散度作为度量  
![图片](images/KL-loss.png)  
MAE loss控制最终年龄的预测，实现为L1距离  
![图片](images/MAE-loss.png)  
总损失为两个loss相加  
4. 我们以三种粒度级别裁剪人脸中心，然后将它们输入到共享的CNN网络中。最后对三尺度人脸图像的瓶颈进行串级处理。  
5. 不适用残差网络，对于小模型残差网络不好，本文使用SE module.  


