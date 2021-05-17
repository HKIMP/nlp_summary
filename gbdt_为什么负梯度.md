![图 1](images/58e42be04a14b3579b01231c3616ffb280f1c2b69fa503890f70c4eaf7cfb2be.png)  

![图 2](images/dd6b9186f7ae726d6ccca32df88fb94cb35e2a76804995ff982dd02839b5deee.png)  

无论损失函数是什么形式，每个决策树拟合的都是负梯度。准确的说，不是用负梯度代替残差，而是当损失函数是均方损失时，负梯度刚好是残差，残差只是特例。









参考：

1. [gbdt的残差为什么用负梯度代替？](https://www.zhihu.com/question/63560633)
2. [梯度提升树中为什么说目标函数关于当前模型的负梯度是残差的近似值？](https://www.zhihu.com/question/60625492)