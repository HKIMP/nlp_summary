1. 需要看bpe论文

tokenizer的本质是分词，提取有意义的wordpiece，又尽可能少，用尽量
少的信息单元来描述无限的组合。

bert采用wordpiece
wordpiece一种实现的方式就是bpe

wordpiece 不等于 bpe

bert采用的是字符级别的BPE编码，直接生成词表文件，官方词表中包含3w左右的
单词，每个单词在词表的位置对应Embedding中的索引，Bert预留了100个[unused]位置，
便于使用者将自己的数据中重要的token手动添加到词表中.

roberta采用的是byte级别的bpe编码，官方词表包好5w多个byte级别的token。merges.txt中
存储了所有的token，而vocab.txt这是谁一个byte到索引的映射，通常频率越高的byte索引越小。
所以转换的过程是，先






参考：
1. [关于transformers库中不同模型的Tokenizer](https://zhuanlan.zhihu.com/p/121787628)
2. [一文读懂BERT中的WordPiece](https://www.cnblogs.com/huangyc/p/10223075.html#_label2)
3. [WordPiece与BPE的区别](https://blog.csdn.net/yftadyz/article/details/107436251?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_title-1&spm=1001.2101.3001.4242)
4. [BERT 中的tokenizer和wordpiece和bpe（byte pair encoding）分词算法](https://blog.csdn.net/az9996/article/details/108858708?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_title-1&spm=1001.2101.3001.4242)
5. [手把手教你用Pytorch-Transformers——部分源码解读及相关说明（一）](https://www.cnblogs.com/dogecheng/p/11907036.html)
6. [bert第三篇：tokenizer](https://blog.csdn.net/iterate7/article/details/108959082)
7. [BERT - Tokenization and Encoding](https://albertauyeung.github.io/2020/06/19/bert-tokenization.html)
8. [BertWordPieceTokenizer vs BertTokenizer from HuggingFace](https://stackoverflow.com/questions/62405155/bertwordpiecetokenizer-vs-berttokenizer-from-huggingface)