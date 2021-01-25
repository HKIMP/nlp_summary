一类是 intents expressed 和 sql 内容不匹配的问题 ->> 引入中间层
一类是 OOV 的问题 ->> pointer network

IRnet思路：
1. 引入中间层
为了解决Mismatch的问题，加入 SemQL 进行过渡。
NL -> SemQL -> SQL




IRnet 总体上分为3步
1. Schema Linking
2. 生成SemQL
3. 从SemQL中推断出SQL

### Model

question, a dataset schema and the schema linking results as input





参考：
1. [Text-to-SQL论文阅读笔记：IRNet](https://zhuanlan.zhihu.com/p/136877103)
2. [Text-to-SQL 中引入中间表示](https://zhuanlan.zhihu.com/p/69821022)