一类是 intents expressed 和 sql 内容不匹配的问题 ->> 引入中间层
一类是 OOV 的问题 ->> pointer network

IRnet思路：
引入中间层
为了解决Mismatch的问题，加入 SemQL 进行过渡。
NL -> SemQL -> SQL


IRnet 总体上分为3步
1. Schema Linking
2. 生成SemQL
3. 从SemQL中推断出SQL

1. Schema Linking:
   对Question进行处理，识别 Table, Column, Value    

   Table, Column识别：
   用n-gram (n=1~6), 枚举出所有的单词集合，如果某个n-gram可以和column
   完全匹配或者部分匹配，则识别为column。识别Tables是同样的方法。如果同时被识别为
   Column和Table，则认为是Column。

   Value的识别：
   使用ConceptNet，把value span 放到Conceptnet进行查询，找到对应的Concept再来跟
   Column对比，如果能匹配上，就能确定Value和Column之间的对应关系。

2. 生成SemQL
   
   2.1 NL Encoder：对Question进行编码
   根据Schema Linking的结果，把question分成若干个spans。把每个span的word embedding和
   span的类型，求平均后作为span的embedding，用一个bi-lstm进行编码之后，将隐层作为输出。

   2.2 Schema Encoder: 对Database Schema 进行编码
   s = (c, t) 表示一个数据库的schema。c为columns, t为table.
   schema 将 s 作为输入，最终输出的是 Ec表示 column, Et表示table

   2.3 Decoder 生成SemQL
    ？？
    怎么和Schema Encoder 结合的啊

3. 生成SQL


### Model

question, a dataset schema and the schema linking results as input





参考：
1. [Text-to-SQL论文阅读笔记：IRNet](https://zhuanlan.zhihu.com/p/136877103)
2. [Text-to-SQL 中引入中间表示](https://zhuanlan.zhihu.com/p/69821022)