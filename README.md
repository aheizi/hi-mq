## 翻译RabbitMQ官方Java教程
1. [RabbitMQ之HelloWorld](http://www.cnblogs.com/aheizi/p/5755021.html)  
2. [RabbitMQ之任务队列](http://www.cnblogs.com/aheizi/p/5778369.html)  
3. [RabbitMQ之发布订阅](http://www.cnblogs.com/aheizi/p/5782469.html) 
4. [RabbitMQ之路由(Routing)](http://www.cnblogs.com/aheizi/p/5785992.html)  
5. [RabbitMQ之主题(Topic)](http://www.cnblogs.com/aheizi/p/5789444.html)
6. [RabbitMQ之远程过程调用(RPC)](http://www.cnblogs.com/aheizi/p/5797703.html)

RabbitMQ是一个由erlang开发的AMQP（Advanced Message Queue ）的开源实现。  

对于一个大型的软件系统来说，它会有很多的组件或者说模块或者说子系统或者（subsystem or Component or submodule）。那么这些模块的如何通信？这和传统的IPC有很大的区别。传统的IPC很多都是在单一系统上的，模块耦合性很大，不适合扩展（Scalability）；如果使用socket那么不同的模块的确可以部署到不同的机器上，但是还是有很多问题需要解决。比如：

1. 信息的发送者和接收者如何维持这个连接，如果一方的连接中断，这期间的数据如何方式丢失？

2. 如何降低发送者和接收者的耦合度？

3. 如何让Priority高的接收者先接到数据？

4. 如何做到load balance？有效均衡接收者的负载？

5. 如何有效的将数据发送到相关的接收者？也就是说将接收者subscribe 不同的数据，如何做有效的filter。

6. 如何做到可扩展，甚至将这个通信模块发到cluster上？

7. 如何保证接收者接收到了完整，正确的数据？

AMDQ协议解决了以上的问题，而RabbitMQ实现了AMQP。[RabbitMQ官网](https://www.rabbitmq.com)
