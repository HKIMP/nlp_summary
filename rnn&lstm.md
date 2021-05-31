## question
lstm只是解决了长期依赖的问题吗，没解决梯度的问题吗？
长期依赖不就是梯度不消失吗

rnn不能捕捉远距离信息，是不是因为bptt，长距离的梯度衰减。近距离的梯度影响大于远距离的梯度。



lstm三个门：
1. 输入门
2. 遗忘门
3. 输出门

recursive recurrent

rnn梯度消失
![图 1](images/97f28e85df4beacbd4ea97afd8003942327886637e9ce055a308a0372e639f6a.png)  
![图 2](images/c4972f5c4fe47612cc98def15ea861d99d3b44255b5656f03b27a0bab0c32e96.png)  

为什么梯度消失是一个问题：
![图 3](images/4d178719a3478d047e742c65df69284da1685499c5cf9f5de88de43a1657e8a9.png)  


