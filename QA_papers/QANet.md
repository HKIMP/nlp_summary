draws inspiration from 'Attention is all you need'
## Motivation
The key motivation behind the design of the model:
1. convolution captures the local struct of the text
2. self-attention learns the global interaction between each pair of words.

## 贡献
The contribution of this paper are as follows:
* Propose an efficient reading comprehension model that exclusively built upon convolutions and self-attentions.

maintains good accuracy and speed up

speed up makes our moedl the most promising candidate for scaling up to larger datasets.

* 模型加速意味着可以处理更多数据，为了提高结果，使用机器翻译扩充了训练集。

## 结构
五层：
1. Input Embedding Layer
2. Embedding Encoder Layer
3. Context-Query Attention Layer
4. Model Encoder Layer
5. Ouyput Layer





## ??
1. 怎么test啊
2.  损失函数
3.  数据怎么转换的

拉取合并
