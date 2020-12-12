transformer是字作为输入 不是词？？
字 词？？

transformer的 位置编码是不训练的 bert的位置编码是训练的


## positional embedding 相关

参考：
1. [如何理解Transformer论文中的positional encoding，和三角函数有什么关系？](https://www.zhihu.com/question/347678607)
2. [Transformer使用position encoding会影响输入embedding的原特征吗？](https://www.zhihu.com/question/350116316)
3. 

$PE{(pos,2i)} = sin(pos / 10000^{2i/d_{\text{model}}}) \\ PE{(pos,2i+1)} = cos(pos / 10000^{2i/d_{\text{model}}})$

绝对位置编码，相对位置编码（三角函数编码）



mask在transformer中，目的有两个
1. 让padding（不够长补0）的部分不参与attention的操作（普通的Scaled Dot-Product Attention）
2. 在decoder input过程中，生成当前词语的概率分布时，让程序不会
   注意到这个词后边的部分。（Masked Multi-Head Attention）






![图一](images/transformer.png)
![图二](images/transformer2.png)

代码：
1. transformer decoder 的input 是真实的 词 还是预测出来的词？
    还是训练的时候, decoder input 用真实的值 类似于 teacher foring
    测试的时候，用预测的值。

    s2s 的训练过程也是真实值作为 decoder 的输入吗

2. QK 的维度必须相等 V的维度可以和他们不等

3. 为什么 scaled dot product attention

4. 哪写非得做mask啊，mask并不是为了减小计算量？而是不为了pad影响其他元素？

5. 


## 参考

(NLPer看过来，一些关于Transformer的问题整理)[https://www.nowcoder.com/discuss/258321]

